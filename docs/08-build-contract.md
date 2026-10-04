# Nelvra — Build Contract

## Objective

Implement the product described by the master blueprint while preserving a clean separation between:

**product logic**
**MJS pilot data**
**tenant/customer configuration**

## Non-negotiable principles

### 1. Action-first

Every major screen must help the operator decide or execute something.

### 2. Ledger-first

Inventory and money-changing events must be traceable to source transactions.

### 3. Offline-first where field reality requires it

An outlet visit should not fail because the connection is temporarily unavailable.

### 4. No false precision

Estimated outlet stock must be visually distinguished from observed stock.

### 5. Auditability

Sensitive stock, collection, pricing, and financial adjustments must preserve an audit trail.

### 6. Configuration over hardcoding

Business thresholds should be configurable where practical.

### 7. MJS is data, not architecture

No MJS-specific product IDs, route assumptions, or business constants should be embedded in core domain logic.

## Minimum technical shape

### Frontend

Mobile-first PWA.

Requirements:

- fast startup
- touch-friendly controls
- low cognitive load
- offline transaction queue
- sync status visibility
- safe retry behavior

### Backend

Cloudflare Workers or equivalent stateless API layer.

Requirements:

- authenticated requests
- authorization checks
- deterministic business rules
- idempotent write handling
- structured errors

### Database

PostgreSQL-compatible relational database.

Requirements:

- tenant isolation
- foreign-key integrity
- transaction-safe writes
- indexed operational queries
- audit records

## Transaction requirements

Inventory-changing and money-changing commands should be idempotent where retries are possible.

Every important transaction should have:

- unique ID
- source operation
- actor
- timestamp
- affected entity
- before/after context when applicable

## Security baseline

- least privilege
- secure session handling
- server-side authorization
- no secrets in repository
- no credentials in seed data
- production environment separation
- backup and restore plan

## Observability baseline

Track:

- API errors
- failed syncs
- rejected transactions
- authorization failures
- background job failures where applicable
- database errors
- client-side sync backlog

## Testing baseline

At minimum:

- domain unit tests
- calculation tests
- inventory movement tests
- collection/settlement tests
- authorization tests
- offline retry/idempotency tests
- migration/integrity tests
- production build verification

## Release gate

A phase is not complete because the UI renders.

A phase is complete when:

**business rule → transaction → persisted state → derived metric → operator action**

works end to end and is covered by tests appropriate to its risk.

## Future productization

Keep clear boundaries so one deployment can later support multiple distributors without rewriting the core domain.

Future configuration areas may include:

- retailer margin model
- visit cadence rules
- route cost allocation
- product units
- pricing model
- approval rules
- inventory policies
- action thresholds
