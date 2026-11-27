# Project Alpha — Status Report

**Reporting date:** 2026-11-20  
**Project owner:** Maya Chen  
**Status:** At risk  
**All project details are fictional.**

## Objective
Deliver a unified merchant reporting dashboard with transaction search, settlement summaries, and export capabilities.

## Progress
- Transaction search: complete.
- Settlement summary: in QA.
- CSV export: complete in staging.
- Role-based report permissions: in development.

## Risks
1. Finance has not finalized the settlement report acceptance criteria.
2. Permission testing found one low-severity issue involving stale browser sessions.
3. The reporting API p95 latency is above the internal target under the largest test dataset.

## Next actions
- Product and Finance to approve acceptance criteria by 2026-11-24.
- Engineering to retest session invalidation by 2026-11-25.
- Platform team to profile report API queries by 2026-11-27.

## Dependencies
The release depends on the identity service permission update and the Finance team's sign-off.
