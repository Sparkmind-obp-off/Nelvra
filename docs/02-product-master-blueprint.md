# Nelvra — Product Master Blueprint

## 1. Product objective

Increase the economic quality of distribution operations by making stock, cash, outlet performance, route effort, and next actions visible in one operational system.

The target is not "more software usage." The target is better business outcomes.

## 2. Core money leaks

Nelvra is designed to address:

1. **Field inventory** — stock outside the base but not yet converted to cash.
2. **Stockouts** — an outlet sells out between visits and loses sales.
3. **Slow/dead stock** — stock remains trapped while receiving more replenishment.
4. **Collection leakage** — money is due at outlets but not visible or prioritized.
5. **Low-value routes** — travel cost and time are spent on weak outlets.
6. **Weak outlet prioritization** — all outlets receive similar attention despite different economics.
7. **SKU economics blindness** — best-selling products may not be the most profitable.
8. **Packing-yield variance** — bulk input does not always convert into the expected number of sellable packs.
9. **Owner dependency** — critical business memory stays in notes, WhatsApp, or memory.

## 3. Core engines

### Stock Engine

Tracks inventory across operational states and locations.

### Outlet Engine

Tracks outlet status, sell-through, due amount, visit pattern, and economic value.

### Collection Engine

Tracks amount due, collected amount, outstanding balance, and collection priority.

### Route Engine

Groups and prioritizes visits according to economic value, due work, restock needs, and route effort.

### Profit Engine

Calculates product, outlet, and route contribution from actual economics.

### Action Engine

Turns business data into the next operational action.

## 4. Primary user journey

### Before the route

The operator opens Nelvra and sees:

- expected collection
- outlets due
- restock quantities
- returns
- priority actions
- route contribution estimate

### During a visit

The operator records only what is needed:

- outlet
- product
- sent
- sold
- remaining
- returned
- amount collected
- new stock placed
- notes only when necessary

Target interaction time: approximately 30–60 seconds per outlet.

### After the route

Nelvra updates:

- field stock
- outlet inventory state
- receivables
- sales velocity
- product contribution
- route economics
- next actions

## 5. MVP scope

### Master data

- Products / SKUs
- Pricing
- Retailer margin
- Outlet master
- Areas
- Users / roles

### Operations

- Production/packing batch
- Stock locations
- Inventory movements
- Outlet allocations
- Visits
- Restock
- Returns
- Collections

### Economics

- unit cost
- selling price
- contribution
- outstanding
- route expense

### Intelligence

- fast / normal / slow / dead
- stockout risk
- collection priority
- outlet priority
- route priority

### Action

- collect
- restock
- stop restock
- revisit
- reactivate
- move stock
- produce / buy

## 6. Explicitly out of scope for v1

- full accounting
- payroll
- marketplace management
- public e-commerce storefront
- customer chatbot
- real-time GPS fleet tracking
- large CRM suite
- complex AI agents
- multi-branch enterprise features

These can be considered only after the core profit loop is validated.

## 7. Decision principle

Every feature must answer at least one of these:

**Does it improve revenue?**

**Does it accelerate cash conversion?**

**Does it reduce cost/leakage?**

**Does it increase inventory efficiency?**

**Does it improve operational control?**

If not, it should not be part of MVP.
