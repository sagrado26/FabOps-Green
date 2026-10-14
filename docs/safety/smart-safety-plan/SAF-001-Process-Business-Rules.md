# SAF-001 — Process & Business Rules v0

**Status:** Draft; proposed behaviours, not an approved safety policy. [Executive PRD](SAF-001-Executive-PRD.md) · [Technical PRD](SAF-001-Technical-PRD.md) · [Decisions](02-decision-register.md)

## Process gates

| Gate | Product behaviour | SAF requirements | Authority still required |
|---|---|---|---|
| Create / resume | Identify task, asset and actor; preserve incomplete draft | 001–003, 023, 027 | Draft ownership and edit permissions |
| Hazard screening | Ask applicable controlled questions; distinguish unanswered; show mappings | 004–007, 021–024 | Approved 12 questions and conditional catalogue |
| Risk assessment | Carry hazards forward; record initial/residual risk, mitigations and obligations | 008–009, 028 | Risk methodology and escalation thresholds |
| Submit | Validate mandatory answers against current task, plan and catalogue context | 010, 023, 027 | Submission policy |
| Review | Record authorized decision, actor, reason and applicable revision | 011, 025, 028–029 | Approval matrix and SRB role |
| Start / restart | Evaluate current applicable prerequisites; explain refusals | 012, 025, 030 | Which PTW/LOTO/acknowledgment gates apply to each transition |
| Change / handover | Detect changed conditions, assess impact, retain history and communicate outstanding actions | 013–015, 017, 027–030 | Revision triggers and reacknowledgment |
| Controlled content | Preview and publish versions without changing historical records | 018, 021–024, 026, 031 | Content steward and publish authority |

## Participant acknowledgment

[BR-058–BR-065](SAF-001-Acknowledgment-Rules.md) define individual acknowledgments, their relation to the Action Lead and separate authorities for review, toolbox talks and work authorization. Mandatory lead acknowledgment and single-person/in-progress exceptions are **candidate policies pending adoption**, not a blanket all-participants gate.

## Exceptions and refusal behaviour

Missing or unknown question/control status cannot be represented as No or verified. Stale revisions, unauthorized review, duplicate submissions, failed integrations and concurrent edits must not display false success. Historical approvals, physical isolation and live permits may have different lifecycles: do not automatically void, close or release them as a side-effect of editing the plan.

## SRB, PTW and LOTO boundaries

- **SRB:** governance of reassessment and board decisions; whether the SRB decision changes the plan revision requires approval.
- **PTW:** plan-derived permit requirement and linked status; actual issuance, expiry, suspension and closure governed separately.
- **LOTO:** identify isolation obligation and reference independently verified evidence; a software plan cannot assert a physical isolation.
- **Readiness:** notices, blocking transitions and already-running work treatment are defined per transition, not by a generic blanket rule.

## Acceptance traceability

Every approval gate must have actor, plan revision, authoritative inputs, relevant requirement IDs, applicable decision ID and negative-path tests. Approval decision and test results must be retained. See [Verification](SAF-001-Verification-Acceptance.md).

**Controlled rule inventory:** [BR-001–065 and SAF-REQ traceability](SAF-001-Business-Rule-Traceability.md) (Draft; no approved safety policy implied).

## Product decisions and unresolved gates — 14 October 2026

The product direction is confirmed for SAF-DEC-001–008 in the [Decision Register](02-decision-register.md). Thus: initial twelve approved configurable questions; chosen severity/likelihood/max-risk model with SRB trigger ≥6; global-plus-local standards applicability; independent linked SRB/PTW/LOTO; open eligible preparation with governed approval and named acknowledgments; Action Lead change assessment subject to mandatory escalation; standard attributable audit; and standard tested Product Owner software acceptance.

**Remaining safety-policy gates:** exact question mappings, formal risk acceptance, board/permit/isolation state transitions, acknowledgment start/restart thresholds, Action Lead mandatory escalations, record retention duties and legally required operational sign-off. No rule should be read to automatically re-gate active work or release physical isolation.
