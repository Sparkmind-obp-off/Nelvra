# PHASE 8 — PRODUCTION HARDENING

## Objective
Turn the working product into software that can safely handle real business operations.

## Security
- authentication hardening
- authorization review
- tenant isolation
- secure session handling
- secret/environment separation
- least privilege
- input validation

## Reliability
- idempotent write commands
- offline queue
- retry handling
- sync conflict behavior
- safe recovery
- transaction atomicity

## Data integrity
- foreign keys
- constrained state transitions
- audit events
- reversal/adjustment mechanisms
- historical reproducibility

## Recovery
- backups
- restore test
- migration rollback strategy
- operational runbook

## Observability
Track:
- API errors
- failed syncs
- rejected transactions
- authorization failures
- database errors
- client backlog
- critical workflow failures.

## Testing
- unit tests
- integration tests
- ledger tests
- calculation tests
- authorization tests
- offline/idempotency tests
- migration tests
- production build checks.

## Deployment
Preferred direction:
- Cloudflare Workers/API
- PostgreSQL/Neon
- production environment separation
- monitored deployments.

## Exit gate — PRODUCTION READY
The system is secure enough for the pilot, operational failures are observable and recoverable, and critical transactions do not depend on manual developer repair.