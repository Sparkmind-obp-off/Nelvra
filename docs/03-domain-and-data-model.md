# Nelvra — Domain & Data Model

## 1. Source of truth

Nelvra should use a transaction-oriented business ledger.

Balances and summaries are derived from recorded business events where practical. Critical inventory and money adjustments require an audit trail.

## 2. Core domain entities

### Tenant

Supports future productization and strict tenant isolation.

### User

Operator identity and role.

Roles initially:

- Owner
- Admin
- Field Operator

### Product

SKU master including:

- name
- category
- unit
- pack weight
- selling price
- retailer margin
- standard cost
- status

### ProductionBatch

Represents bulk-to-pack conversion.

Key fields:

- raw product
- raw quantity
- raw cost
- packaging cost
- expected yield
- actual yield
- unit cost
- production date

### StockLocation

Examples:

- raw material
- packing stock
- ready stock
- vehicle
- outlet

### InventoryMovement

Immutable operational movement:

- product
- quantity
- from location
- to location
- movement type
- source transaction
- timestamp
- operator

### Outlet

Includes:

- name
- owner/contact
- area
- location
- status
- visit cadence
- notes

### OutletAllocation

Represents stock currently entrusted to an outlet.

Should distinguish:

- observed quantity
- sold quantity
- returned quantity
- estimated remaining quantity
- last observed timestamp

The system must not pretend that consignment stock is real-time when the outlet is only observed periodically.

### Visit

Records an outlet visit and the work done.

### Settlement / Collection

Represents cash due and cash collected.

Must support:

- amount due
- amount collected
- collection date
- outstanding
- reference/source

### Route

A visit plan with:

- date
- outlets
- priority
- estimated effort
- estimated collection
- route expense

### Expense

Operational expense such as fuel or route-related spend.

### Action

Machine/system recommendation or operator action.

Examples:

- collect
- restock
- stop restock
- revisit
- reactivate
- move stock
- produce
- buy

### AuditEvent

Records who changed what, when, and the before/after context for sensitive records.

## 3. Inventory state model

Conceptual flow:

RAW MATERIAL
→ PACKING STOCK
→ READY STOCK
→ VEHICLE
→ OUTLET
→ SOLD / RETURN

"Field inventory" is the total of stock outside the base that is not yet settled as sold cash.

## 4. Economics model

### Unit contribution

Selling price
− unit COGS
= gross contribution per unit

### Outlet contribution

Outlet gross contribution
− attributable route/service cost
= outlet contribution

### Route contribution

Route gross contribution
− route expenses
= route contribution

The system should not allocate cost with false precision. Cost allocation methods must be configurable and transparent.

## 5. Data-quality rules

- Negative stock is blocked unless an explicitly controlled adjustment flow exists.
- Financial/inventory corrections are audited.
- Estimated field stock must be distinguished from observed stock.
- Deleted transactional records should be avoided; use reversal/adjustment events where practical.
- Historical economics must remain reproducible.
