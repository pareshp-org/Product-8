# UAT Runbook — Product-8 (Asynchronous Job Orchestration)

## Feature
Background task queueing, execution and status tracking

## Preconditions
- Service is configured with valid environment (`.env.local` or `.env.example`).
- Database migrations have been applied via `make migrate`.
- Required port is free and accessible.

## Steps
1. Start Product-8 on port 8088
2. Schedule background job via POST /api/v1/jobs
3. Query job status via GET /api/v1/jobs

## Expected Results
- Job accepted with job ID and 'scheduled' status
- Job execution completes and status reflects success

---
*Author: QA & Primary Owner (MasterSpec Section 31.1, Section 33.1)*
*Verification Contract: `verification/contract.yaml`*
