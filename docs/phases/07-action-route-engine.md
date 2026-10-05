# PHASE 7 — ACTION & ROUTE ENGINE

## Objective
Convert signals into prioritized decisions the operator can execute immediately.

## Action vocabulary
- COLLECT
- RESTOCK
- STOP RESTOCK
- VISIT
- REVISIT
- REACTIVATE
- MOVE STOCK
- PRODUCE
- BUY

## Priority inputs
Actions may consider:
- amount due
- overdue age
- stockout risk
- sell-through
- outlet contribution
- product contribution
- field stock age
- restock requirement
- route expense
- area clustering.

## Route strategy
Start with economic prioritization and area clustering.

Do not make complex GPS/TSP optimization a prerequisite for value.

## Next Best Action
The system should generate a ranked queue of actionable work with a short reason.

Example format:
**COLLECT — Outlet A**
Reason: outstanding amount is due today.

**RESTOCK — Outlet B**
Reason: recent sell-through exceeds configured threshold and stockout risk is rising.

**STOP RESTOCK — SKU C**
Reason: sustained weak movement and high field stock.

## Human control
Recommendations remain explainable and overrideable. An operator can reject or change an action, and the action result becomes part of the history.

## Exit gate — ACTION OPERATIONAL
Important economic signals produce a ranked action queue and a route plan that the operator can execute.