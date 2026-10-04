# Nelvra — Full Master Roadmap

## Product
**NELVRA — Distribution Profit System**

Core principle: **Dashboard is not the product. Action is the product.**

Core business loop:
BUY → PACK/PRODUCE → DISTRIBUTE → OUTLET → SELL-THROUGH → COLLECT → RESTOCK → REPEAT → PROFIT

MJS Snack is the first design partner and operational pilot.

## Roadmap overview

| Phase | Name | Primary Outcome | Exit Gate |
|---|---|---|---|
| 0 | Foundation & Preflight | Canonical project foundation | Foundation Ready |
| 1 | Master Vision | One locked product vision and boundary | Vision Locked |
| 2 | Profit Discovery | Verified MJS economics and workflows | Discovery Validated |
| 3 | System Architecture | Domain, ledger, calculations, permissions | Architecture Locked |
| 4 | UX & Operational Design | Field-first workflows | UX Validated |
| 5 | Distribution Core | End-to-end operational system | Core Operational |
| 6 | Profit Intelligence | Economic visibility and risk detection | Intelligence Useful |
| 7 | Action & Route Engine | Prioritized actions and route economics | Action Operational |
| 8 | Production Hardening | Security, reliability, offline, audit, observability | Production Ready |
| 9 | MJS Operational Pilot | Real-world measured validation | Pilot Validated |
| 10 | Productization | Reusable product for other distributors | Product Ready |

## PHASE 0 — FOUNDATION & PREFLIGHT
Create one source of truth for brand, product, architecture, pilot, constraints, and definition of done.
Scope: repository structure, documentation, brand status, product category, master blueprint, domain/data direction, MJS pilot definition, implementation contract, explicit non-goals.
Exit gate: all core product decisions are documented and no unresolved contradiction blocks Phase 1.

## PHASE 1 — MASTER VISION
Define exactly what Nelvra is, who it serves, the economic problem it owns, how it creates value, and what it must never become.
Scope: product thesis, customer, money cycle, four product layers, core engines, product boundaries, north-star outcomes, UX principles, brand direction, feature decision filter.
Deliverable: canonical Phase 1 Master Vision document.
Exit gate: the product can be explained in one sentence, the business loop and MVP boundary are explicit, and later features can be tested against this vision.

## PHASE 2 — PROFIT DISCOVERY
Replace assumptions with actual MJS data and validated operating behavior.
Inputs: SKU list, bulk/bale cost, packaging cost, packing yield, selling price, retailer margin, outlets, geography, cadence, sent/sold/return quantities, collections, outstanding, route/fuel cost, production time, slow/dead stock evidence.
Deliverables: verified business model, money-leak map, baseline metrics, validated workflows, initial thresholds, unresolved-data list.
Exit gate: no critical product rule depends on an unverified assumption.

## PHASE 3 — SYSTEM ARCHITECTURE
Turn the validated business model into a deterministic and auditable system.
Core domain: Tenant, User, Product, ProductionBatch, StockLocation, InventoryMovement, Outlet, OutletAllocation, Visit, Settlement, Collection, Route, Expense, Action, AuditEvent.
Core rules: inventory ledger, field inventory, collection/receivable model, COGS, contribution, stock velocity, permissions, tenant boundaries, correction/reversal, audit.
Exit gate: domain model, calculations, permissions and transaction rules are internally consistent and testable.

## PHASE 4 — UX & OPERATIONAL DESIGN
Design around real owner/operator behavior, especially field visits.
Primary surfaces: Home, Outlet Visit, Owner Control Surface.
Requirements: mobile-first, low cognitive load, touch-friendly, offline-first where required, clear sync status, short forms, observed versus estimated stock clearly differentiated.
Exit gate: a real operator can complete common workflows quickly without documentation.

## PHASE 5 — DISTRIBUTION CORE
Build the operational backbone.
Modules: auth/roles, products/pricing, production/packing, stock locations/movements, field inventory, outlets/allocations, visits, restock, returns, settlements, collections, basic route planning.
Definition of done: production → ready stock → vehicle → outlet → sell-through → collection → restock works end-to-end with persistent history and auditability.
Exit gate: critical distribution path works with appropriate tests.

## PHASE 6 — PROFIT INTELLIGENCE
Expose where economic value is created, trapped, or lost.
Engines: product economics, outlet economics, inventory intelligence, collection intelligence.
Outputs: contribution, sell-through, velocity, aging, stockout risk, field inventory value, due/overdue, days-to-cash.
Exit gate: owner can answer what sells, what makes money, where cash is stuck, where stock is stuck, and which outlets deserve attention.

## PHASE 7 — ACTION & ROUTE ENGINE
Turn insights into prioritized operational decisions.
Actions: COLLECT, RESTOCK, STOP RESTOCK, VISIT, REVISIT, REACTIVATE, MOVE STOCK, PRODUCE, BUY.
Route priority uses outstanding, stockout risk, sell-through, outlet contribution, restock need, area clustering and route cost.
Do not build complex GPS/TSP optimization before route economics are proven.
Exit gate: important signals produce clear next actions that the operator can execute.

## PHASE 8 — PRODUCTION HARDENING
Make Nelvra safe and reliable as real business software.
Scope: authentication, authorization, least privilege, secrets, tenant isolation, idempotent writes, offline queue, retries, conflict handling, audit, backups, restore verification, monitoring, error tracking, performance, deployment and security/integrity testing.
Exit gate: ordinary operational recovery does not require developer intervention.

## PHASE 9 — MJS OPERATIONAL PILOT
Prove whether the product produces measurable business value in real MJS operations.
Method: Baseline → Controlled Use → Compare → Refine.
Metrics: sell-through, stockout frequency, slow/dead stock value, collection cycle, route contribution, outlet contribution, inventory turnover, visit time, reconciliation error rate.
Rule: no guaranteed percentage improvement before baseline and pilot evidence exist.
Exit gate: measurable value with acceptable operator workload and reliable transaction integrity.

## PHASE 10 — PRODUCTIZATION
Turn the validated MJS system into a reusable product.
Scope: multi-tenant architecture, configurable rules, onboarding, tenant settings, reusable templates, deployment automation, billing/subscription model, support documentation, analytics and customer health.
Principle: MJS-specific data becomes configuration; core business logic remains reusable.
Exit gate: a second distributor can onboard without forking the core architecture.

## GLOBAL DEFINITION OF DONE
Nelvra is not complete because screens render.

Business rule → User action → Transaction → Persisted state → Derived metric → Operational decision

Critical paths must be understandable, testable, auditable, recoverable, and measurable.

## MASTER PRODUCT FILTER
Every core feature must plausibly improve at least one of:
1. Revenue
2. Cash conversion
3. Cost or leakage
4. Inventory efficiency
5. Operational control
If none apply, the feature does not enter the core product without an explicit product decision.