# PHASE 4 — UX & OPERATIONAL DESIGN

## Objective
Design an interface that follows the operator's real work instead of forcing the operator to think in database structures.

## Experience hierarchy
1. What needs attention now?
2. What money is due?
3. What stock needs movement?
4. Which outlet should be visited?
5. What should happen next?

## Home screen
Primary blocks:
- expected collection
- outlets due
- restock requirement
- priority actions
- route start
- sync status

## Outlet visit
Target flow:
OPEN → CHECK → SELL-THROUGH → RESTOCK/RETURN → COLLECT → SAVE → NEXT

Target interaction time: approximately 30–60 seconds for routine visits.

## Owner control surface
Show:
- cash/outstanding
- field inventory
- top/bottom products
- top/bottom outlets
- route contribution
- exceptions
- prioritized actions

## UX rules
- mobile-first
- touch-first
- large numeric hierarchy
- short forms
- offline-first where field reality requires it
- visible pending-sync state
- observed vs estimated stock clearly separated
- no decorative dashboard noise

## Failure behavior
Temporary loss of connectivity must not silently lose a transaction. Pending transactions need explicit local state, safe retry, idempotency and a visible sync outcome.

## Exit gate — UX VALIDATED
A real operator can perform the main field and owner workflows without training-heavy procedures, and the interface exposes the next action clearly.