# PHASE 3 — SYSTEM ARCHITECTURE

## Objective
Convert the validated MJS workflow into a deterministic, auditable, reusable system architecture.

## Core domain
- Tenant
- User
- Product
- ProductionBatch
- StockLocation
- InventoryMovement
- Outlet
- OutletAllocation
- Visit
- Settlement
- Collection
- Route
- Expense
- Action
- AuditEvent

## Ledger principle
Important stock and money events are represented as transactions. Derived balances and summaries should be reproducible from the underlying record wherever practical.

## Inventory state model
RAW MATERIAL → PACKING → READY STOCK → VEHICLE → OUTLET → SOLD / RETURN

Field inventory means stock outside the base that has not yet become settled cash.

## Core calculations
### Unit contribution
Selling price − unit COGS = gross contribution.

### Sell-through
Units sold ÷ units made available for sale over a defined period.

### Outlet contribution
Gross contribution attributable to an outlet − attributable service/route cost.

### Route contribution
Route gross contribution − route expenses.

## Transaction requirements
- unique transaction ID
- actor identity
- timestamp
- source operation
- entity reference
- idempotency where retry is possible
- audit trail for sensitive corrections

## Security model
- role-based authorization
- least privilege
- tenant isolation boundary
- no production secrets in source
- explicit correction/reversal flows

## Exit gate — ARCHITECTURE LOCKED
The domain model, ledger, formulas, permissions and transaction semantics are documented and can be implemented without inventing core business rules during coding.