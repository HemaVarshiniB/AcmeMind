# Production Deployment Runbook

**Service:** Payment Orchestrator  
**Owner:** Platform Engineering  
**Change window:** Tuesday or Thursday, 18:00–20:00 UTC, unless an emergency change is approved.

## Preconditions
- Change ticket approved by service owner.
- CI pipeline is green.
- Database migration has been reviewed and tested.
- Rollback image and configuration are available.
- On-call engineer is assigned.

## Deployment
1. Announce the deployment in the release channel.
2. Deploy to one canary instance.
3. Observe error rate, latency, and queue depth for 10 minutes.
4. Increase traffic gradually if health checks pass.
5. Complete rollout and run smoke tests.

## Rollback triggers
- HTTP 5xx rate exceeds 2% for 5 consecutive minutes.
- p95 API latency exceeds 1.5 seconds for 10 minutes.
- Payment authorization success rate drops by more than 5 percentage points against the baseline.
- Ledger consistency checks fail.

## Rollback
Stop rollout, restore the previous image, verify service health, and notify the incident commander. Do not reverse a database migration without explicit database-owner approval.

## Post-deployment
Attach deployment logs, dashboard links, test evidence, and any follow-up actions to the change ticket.
