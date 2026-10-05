# PHASE 0 — FOUNDATION & PREFLIGHT

## Objective
Establish the canonical project foundation before business or implementation decisions are allowed to drift.

## Scope
- repository identity and documentation structure
- current brand status and clearance boundary
- product category and positioning
- MJS design-partner role
- technical direction
- implementation contract
- non-goals and feature filter
- definition-of-done convention

## Canonical references
- `docs/01-brand-platform.md`
- `docs/02-product-master-blueprint.md`
- `docs/03-domain-and-data-model.md`
- `docs/04-pilot-and-metrics.md`
- `docs/05-implementation-roadmap.md`
- `docs/06-brand-lock-gate.md`
- `docs/07-brand-look.md`
- `docs/08-build-contract.md`

## Decisions
Project name: NELVRA.
Product category: Distribution Profit System.
Initial design partner: MJS / Mitra Jaya Snack.
Project domain: `nelvra.biz.id`.
Preferred stack: mobile-first PWA, Cloudflare Workers, PostgreSQL/Neon.

## Constraints
- Do not build a generic portal.
- Do not hardcode MJS-specific assumptions into reusable domain logic.
- Do not claim profit uplift before pilot evidence.
- Do not make AI a dependency for core value.
- Do not expand scope without an economic justification.

## Exit gate — FOUNDATION READY
The repository has a stable source of truth, a defined product boundary, known assumptions, and a phase-by-phase execution contract.