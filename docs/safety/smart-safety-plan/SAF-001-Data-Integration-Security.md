# SAF-001 — Data, Integrations & Security v0

**Status:** Draft; logical model only, no imposed stack or database schema. [Technical PRD](SAF-001-Technical-PRD.md)

## Logical information model

| Record | Minimum information / relationship |
|---|---|
| Safety Plan | Stable identity, task, asset, current revision, lifecycle |
| Plan Revision | Assessed work-context snapshot, created actor/time, status |
| Pre-task Question Definition | Stable ID, controlled version, applicability, visibility rules |
| Answer | Question/version, response (including unanswered), recorded actor/time |
| Hazard Selection | Hazard/catalogue version, originating question, task-specific additions |
| Risk Assessment | Hazard, initial assessment, mitigation, residual assessment, method revision |
| Control Obligation | Type/source, responsible party, required/pending/verified/unknown status and evidence reference |
| Approval / SRB Decision | Authorized person/party, decision, reason, plan revision, timestamp |
| Participant Acknowledgment | Named person, plan revision, timestamp and reacknowledgment state |
| Linked PTW / LOTO | External record identity, authoritative status, verification context |
| Event / Audit Record | Change, actor, time, result, version/causation and evidence location |

Do not assume a physical check happened because a boolean or UI field was selected.

## Integration contract

Task and equipment provide current context; Workforce/Identity provides authenticated role and eligibility; PTW, LOTO and SRB supply their independently controlled outcomes; Materials can surface work-relevant hazardous substances and changes; Operations receives handover information; ACOS receives auditable change signals.

Each integration must specify ownership, read/write boundaries, freshness, failure response, replay/deduplication and allowed disclosure. Missing/unknown integration data must never be converted to an affirmative safety status.

## Security, privacy and records

Enforce authorization beyond presentation controls; attribute decisions to authenticated people; segregate acknowledgment from review and start-work permission. Apply least privilege and protect personal, safety and equipment information. Define retention, access/export, correction process, immutable decision history, backup, restoration and site/jurisdiction data-handling requirements with accountable records owners.

## Concurrency and change integrity

Reject stale approvals and contradictory writes; retain recoverable drafts; do not erase answers merely because conditional fields become hidden. Detect differences between a plan revision and current operational context before claiming a successful transition.

## Open contracts

Exact schema, approved risk method, record retention schedule, signature requirements, jurisdictional basis, integration availability and event semantics require separate approval. Related SAF-REQ: 001–002, 007–015, 017–030, 032.
