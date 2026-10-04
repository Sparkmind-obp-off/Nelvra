# Nelvra — MJS Pilot & Metrics

## 1. Pilot role

MJS is the first design partner for validating whether Nelvra can improve a real consignment-based local distribution operation.

The pilot should measure outcomes before making performance claims.

## 2. Baseline discovery

Capture actual data for:

- product list
- retail pack size
- bulk/bale cost
- packaging cost
- current selling price
- retailer margin
- outlet list
- average visit interval
- units placed
- units sold
- units returned
- cash collected
- outstanding
- fuel and route expenses
- production yield
- slow/dead products

Do not hardcode hypothetical sample values into the production rules.

## 3. Leading metrics

### Sell-through

How much of placed stock is sold in a defined period.

### Stockout frequency

How often outlets reach zero before the next visit.

### Slow/dead stock value

Value tied in products with weak movement.

### Collection cycle

Time from outlet sale/settlement due to actual cash collection.

### Route contribution

Economic contribution after route expenses.

### Outlet contribution

Contribution after attributable service/visit cost where measurable.

### Inventory turnover

How efficiently stock converts back into sales/cash.

### Visit time

Average time required to complete one outlet visit.

### Reconciliation error rate

Difference between expected and actual stock/cash during checks.

## 4. Pilot hypothesis

Nelvra is successful if, after a controlled pilot period, the business shows measurable improvement in several of these metrics without creating excessive operator workload.

No guaranteed percentage improvement should be promised before the baseline exists.

## 5. Pilot operating loop

### Stage A — Observe

Capture the current manual process.

### Stage B — Model

Create products, outlets, routes, stock states, costs, and collections.

### Stage C — Operate

Use Nelvra for actual visits, restock, returns, and collection.

### Stage D — Compare

Compare against baseline metrics.

### Stage E — Refine

Adjust thresholds, workflows, and calculations.

## 6. Pilot acceptance criteria

The pilot should demonstrate:

- accurate field stock representation
- reliable collection tracking
- usable outlet priority
- useful next actions
- low-friction field entry
- stable offline/sync behavior where needed
- reproducible profit calculations
- clear owner visibility

Only after these are proven should the product be generalized for external customers.
