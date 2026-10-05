# PHASE 5 — DISTRIBUTION CORE

## Objective
Implement the minimum end-to-end operational loop that turns physical distribution activity into reliable digital records.

## Build order
### 1. Identity
- authentication
- role assignment
- tenant boundary

### 2. Master data
- products
- pricing
- retailer margin
- outlets
- areas

### 3. Production
- production/packing batch
- input quantity
- actual yield
- packaging cost
- unit cost

### 4. Stock
- stock locations
- movement ledger
- ready stock
- vehicle stock
- field/outlet stock

### 5. Outlet operations
- outlet allocation
- visit
- sell-through record
- restock
- return

### 6. Money
- settlement
- collection
- outstanding

### 7. Route
- due queue
- simple route grouping
- route expense capture

## End-to-end acceptance path
Production → Ready Stock → Vehicle → Outlet → Sell-through → Collection → Restock.

## Integrity rules
- no silent negative stock
- sensitive corrections are auditable
- duplicate retries do not double-post
- transaction history is preserved
- calculations use recorded source data

## Tests
- product and price tests
- production yield tests
- inventory movement tests
- outlet allocation tests
- visit/return/restock tests
- collection/settlement tests
- authorization tests

## Exit gate — CORE OPERATIONAL
The critical distribution loop works end-to-end in a controlled environment with reliable persistence and tests.