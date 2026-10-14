# SAF-001 — Verification & Acceptance Plan v0

**Status:** Draft. Evidence is not yet executed. [Technical PRD](SAF-001-Technical-PRD.md) · [Workflow diagrams](SAF-001-User-Workflows.md)

## Acceptance scenarios

| Test ID | Scenario | Primary requirements | Expected outcome |
|---|---|---|---|
| SAF-T01 | Create task-linked plan; resume incomplete draft | 001–003, 023 | Preserved correct task, draft and entered values |
| SAF-T02 | Screen all approved questions; unanswered and conditional responses | 004–007, 021–024 | Correct question visibility, mappings and no hidden-answer loss |
| SAF-T03 | Add task-specific hazard and assess risk | 006–009, 028 | Traceable initial/residual risk using approved method |
| SAF-T04 | Submit incomplete, invalid or stale plan | 010, 015, 027 | Refusal with clear reason; no false approval |
| SAF-T05 | Authorized approval, denial and revision | 011, 013–015, 025 | Correct actor/revision history and controlled reassessment |
| SAF-T06 | Missing/expired/unknown PTW, LOTO, competency or SRB input | 009, 012, 025, 029–030 | Approved transition-specific outcome; no fabricated verification |
| SAF-T07 | Solo Action Lead acknowledgment | 017, 030, BR-058–065 | Outcome matches adopted participation rule |
| SAF-T08 | Multiple named engineers and late joiner | 017, 030, BR-058–065 | Individual traceable acknowledgment; no proxy recording |
| SAF-T09 | Plan revision, shift transfer, task already in progress | 013–014, 017, 030 | Review/acknowledgment requirements according to adopted policy |
| SAF-T10 | Governed template edit, preview and publish | 018, 021–024, 026, 028 | Previous approved plan history unchanged |
| SAF-T11 | Concurrent edits, retry and service outage | 015, 027 | Consistent state, recoverable data, no duplicate decision |
| SAF-T12 | Task Workspace integration, accessibility and notifications | 016, 019–020, 031–032 | Single accessible canonical journey and trustworthy status |

## Evidence per case

Record build/reference, scenario inputs, applicable catalogue/risk version, actor and role, expected versus actual result, test environment, reviewer, defects and linked artifacts. Safety and physical checks need qualified operational validation; a UI demonstration is not proof.

## Release gates

1. Product and safety requirements/decisions approved.
2. Hazard and risk content independently validated.
3. Authorization, permit, isolation and participant gates tested against the applicable transition policy.
4. Negative paths, concurrency, stale state and fail-safe cases proven.
5. Accessibility, operational recovery, security and audit verified.
6. Independent release authority accepts evidence and scope.

**Current conclusion:** Documentation draft prepared; no executed evidence, legal compliance finding, qualified field verification or operational release approval.
