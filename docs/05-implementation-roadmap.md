# Nelvra — Implementation Roadmap

## PHASE 0 — Profit Discovery

Goal: understand the actual MJS money cycle before coding business assumptions.

Deliverables:

- product economics
- production/packing yield model
- outlet inventory model
- collection model
- route cost model
- baseline metrics
- validated workflows

## PHASE 1 — Distribution Core

Build:

- authentication and roles
- products
- outlets
- production batches
- stock locations
- inventory movements
- field stock
- visits
- restock
- returns
- collections

## PHASE 2 — Profit Engine

Build:

- COGS
- gross contribution
- sell-through
- outlet profitability
- product profitability
- slow/dead stock rules
- outstanding aging

## PHASE 3 — Route Intelligence

Build:

- due outlet queue
- economic priority
- collection priority
- restock priority
- route cost capture
- route contribution
- area clustering

Avoid prematurely building a complex travelling-salesman/GPS optimizer.

## PHASE 4 — Action Engine

Build:

- next best action
- stockout risk
- slow-stock alerts
- reorder/restock suggestions
- outlet reactivation
- visit-frequency recommendations
- stock movement suggestions

## PHASE 5 — Production Hardening

Build and verify:

- offline-first transaction queue where field usage requires it
- reliable sync and conflict handling
- audit trails
- authorization
- backups
- monitoring
- error recovery
- performance
- deployment
- onboarding

## PHASE 6 — MJS Operational Pilot

Run the system against real MJS operations.

Measure:

- sell-through
- stockouts
- dead stock
- collection cycle
- route contribution
- outlet contribution
- inventory turnover
- visit time
- reconciliation accuracy

## PHASE 7 — Productization

After validation:

- tenant isolation
- configurable business rules
- onboarding flow
- deployment automation
- subscription packaging
- reusable templates
- documentation
- support process

## Technical direction

Preferred stack:

- mobile-first PWA
- Cloudflare Workers
- PostgreSQL / Neon
- role-based authentication
- offline transaction queue
- server-side calculation layer
- immutable/auditable business ledger

The architecture must keep business rules independent from the MJS-specific seed data.
