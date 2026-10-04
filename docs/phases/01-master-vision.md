# PHASE 1 — MASTER VISION

## Nelvra
**NELVRA — Distribution Profit System**

Status: VISION PHASE

This is the canonical vision contract. Later phases must not contradict it without an explicit product decision.

## 1. Problem we own
Local distributors can lose economic value because the relationship between stock, outlets, sales, collection, route effort and profit is not visible as one operating loop.

Nelvra exists to make that distribution money cycle visible, measurable and actionable.

## 2. Product thesis
> Nelvra helps distributors move stock faster, recover cash sooner, and spend operating effort where it creates the most value.

## 3. Core business loop
BUY → PACK/PRODUCE → DISTRIBUTE → OUTLET → SELL-THROUGH → COLLECT → RESTOCK → REPEAT → PROFIT

Nelvra monitors the whole loop rather than a single department.

## 4. Product category
### Distribution Profit System

Four layers:
- Distribution: products, production, stock, outlets, visits, routes, returns
- Profit: COGS, contribution, collection, outstanding, route/outlet economics
- Intelligence: velocity, stockout risk, slow/dead stock, priority
- Action: collect, restock, stop, visit, move, reactivate, produce, buy

## 5. Core promise
Primary:
> Know where your stock is. Know where your money is. Know what to do next.

Commercial:
> Move stock faster. Recover cash sooner. Move the profit.

## 6. Customer
Initial design partner: MJS / Mitra Jaya Snack.

Future market: snack distributors, FMCG distributors, beverages, frozen food, local wholesalers and small regional distributors.

The architecture must not depend on snack-specific behavior.

## 7. Primary user
The owner/operator who buys or produces stock, packs it, distributes it, visits outlets, checks sell-through, collects money and decides what to restock, produce or buy.

Product principle:
> The system must be faster to use than maintaining the business manually.

## 8. Product jobs
### Know the stock
Where inventory is, how much is at the base, how much is in field stock, how much is at outlets, what is slow, and what is at risk.

### Know the money
What is due, what is collected, what is outstanding, and how quickly stock becomes cash.

### Know what performs
Which products move, which outlets contribute, and which routes justify their cost.

### Detect problems early
Stockout risk, stuck inventory, weak outlets and overdue collection.

### Tell the operator what to do
Prioritize the next action rather than merely displaying data.

## 9. Action-first principle
The home screen should answer: **What should I do next?**

Examples:
- COLLECT — outlet with money due
- RESTOCK — outlet with proven movement
- STOP RESTOCK — slow product/outlet
- VISIT FIRST — high-risk or high-value outlet
- REACTIVATE — declining outlet

This is the defining behavioral difference from a generic business dashboard.

## 10. What Nelvra is not
- generic ERP replacement
- POS replacement
- full accounting suite
- delivery tracker
- fleet management system
- generic CRM
- marketplace
- public web portal
- AI agency
- AI dashboard whose value depends on generated summaries

AI may enhance the product later. Core economic value must exist without AI.

## 11. North-star outcomes
Nelvra should improve:
- revenue
- cash conversion speed
- inventory efficiency
- route productivity
- operating control

## 12. Core metrics
- sell-through
- stockout frequency
- field inventory value
- slow/dead stock value
- collection cycle
- outstanding value
- product contribution
- outlet contribution
- route contribution
- inventory turnover
- visit time
- reconciliation accuracy

Do not promise percentage improvement before baseline measurement.

## 13. Product architecture
Distribution → Profit → Intelligence → Action

Core engines:
Stock → Outlet → Collection → Route → Profit → Action

## 14. Master product loop
DATA → CALCULATION → DECISION → ACTION → RESULT → NEW DATA

The core should use deterministic calculations and rules. AI is optional enhancement, not a dependency.

## 15. Experience principles
- Field-first
- Low-friction
- Offline-first where field reality requires it
- Clear uncertainty between observed and estimated stock
- Numbers first
- Quiet confidence

Common outlet work should target approximately 30–60 seconds without sacrificing transaction integrity.

## 16. Brand direction
**NELVRA**

Personality: calm, precise, practical, commercial, mature, quietly confident.

Descriptor: **Distribution Profit System**

Pilot relationship: **NELVRA for MJS Snack**

Future architecture: **NELVRA for Distribution**

Visual direction: movement + control + clarity.

Avoid literal truck, warehouse, barcode, coin or snack symbolism.

## 17. Feature decision filter
Every core feature must plausibly improve at least one:
- Revenue
- Cash conversion
- Cost/leakage
- Inventory efficiency
- Operational control

If none apply, the feature stays outside the core product unless explicitly approved.

## 18. MVP vision
The first usable version must support the critical loop:

Create product → record production/packing → move stock → assign to outlet → visit outlet → record sell-through/return → collect → replenish → see contribution → receive prioritized next actions.

Everything outside this loop is secondary.

## 19. Long-term vision
Nelvra becomes the operating layer between physical distribution activity and business decisions.

The owner should not need to repeatedly ask:
- Where is my stock?
- Who owes me?
- Where should I go?
- What should I restock?
- Which product actually makes money?
- Where am I wasting time?

The system should make those answers continuously visible and actionable.

## 20. Phase 1 exit criteria
Phase 1 is VISION LOCKED when the following remain stable:
- Nelvra = Distribution Profit System
- Target = local distributors with field/outlet operations
- Problem = economic control of the distribution money cycle
- Optimization = revenue, cash conversion, inventory efficiency, route productivity, operating control
- Defining behavior = business data becomes the next profitable action
- Boundary = do not become a bloated ERP or passive dashboard

Once these are locked, Phase 2 may introduce validated MJS facts and data-driven business rules without changing the core vision.