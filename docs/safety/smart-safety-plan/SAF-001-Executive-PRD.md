# SAF-001 — Smart Safety Plan: Executive PRD

| Field | Value |
|---|---|
| Product | FabPilot / FabOps-Green |
| Function | Safety |
| Version | 0.5 — Draft |
| Date | 14 October 2026 |
| Status | **Not approved for implementation or safety use** |
| Accountable owner and approvers | To be assigned |
| Detailed specification | [SAF-001 Technical PRD](SAF-001-Technical-PRD.md) |

## Executive summary

The Smart Safety Plan embeds hazard identification, risk assessment and safety planning into a maintenance task. Engineers should be able to prepare work efficiently while seeing relevant hazards, baseline controls and outstanding obligations in context. Safety reviewers should have a clear record of what was assessed, what controls are required and which decisions remain unresolved.

The Safety Plan is a **digital planning and authorization workflow**, not proof that physical safeguards, equipment isolation or permits have been implemented.

## Problem and business outcomes

- Reduce duplicated entry and unnecessary administration during maintenance preparation.
- Improve consistency of hazard identification and task-specific mitigation.
- Make safety obligations visible to the people carrying out work.
- Maintain traceable reviews, approvals and revisions when work conditions change.
- Support multi-person and multi-shift maintenance without losing safety context.
- Connect safety readiness to task execution without creating separate competing workflows.

Success measures will include preparation and review effort, completeness and quality of risk assessments, rework after material changes, outstanding obligations, and blocked unsafe start attempts. Baselines and numerical targets are not yet approved.

## Users and responsibilities

| User | Primary need |
|---|---|
| Field Service Engineer | Create, save, complete and revise a plan |
| Task Lead | Coordinate team participation and scope |
| Safety Reviewer / Approver | Review risks and controls and record authorized decisions |
| Operations | See readiness and scheduling implications |
| Participating Engineer | Understand and acknowledge applicable plan and obligations |
| Configuration Steward | Manage approved hazard questions and templates without rewriting prior decisions |

Precise role permissions and approval authority require formal definition.

## Four-stage experience

1. **Task Details:** use the task, equipment, people and work context as the basis for planning; minimise re-entry.
2. **Hazard Identification:** guide users through an intended **12-question screening experience**. Relevant responses reveal selectable hazards and concise contextual guidance. The exact approved questions and mappings remain to be established.
3. **Risk Assessment:** carry selected hazards into a single governed risk-assessment process, including unwanted events, consequences, controls, mitigation and residual risk.
4. **Review & Approval:** show a clear summary, outstanding obligations, approvals and the impact on task readiness.

The experience should be compact, accessible and responsive, with critical safety information available at the point of work.

## Core capabilities

| Capability | Expected outcome | Technical requirement references |
|---|---|---|
| Task-linked planning | One consistent create/edit/review journey tied to task and equipment | SAF-REQ-001–003, 020, 032 |
| Hazard guidance | Contextual screening, approved questions, hazard selection and additional hazards | SAF-REQ-004–007, 021 |
| Risk and controls | One controlled method for initial/residual risk and applicable obligations | SAF-REQ-008–009, 025, 029–030 |
| Trusted review | Authorized submission, decisions, readiness and safe handling of changed conditions | SAF-REQ-010–015, 023, 027–028 |
| Usability and collaboration | Accessible workflow, handover awareness, clear controlled icons | SAF-REQ-016–017, 031 |
| Governed configuration | Versioned reusable templates, conditional forms and preserved answers | SAF-REQ-018, 022, 024, 026 |
| Coordination | Auditable ACOS events and notifications | SAF-REQ-019 |

These reference IDs are **draft**, not signed-off mandatory controls. The [Technical PRD](SAF-001-Technical-PRD.md) holds the full requirements table and acceptance criteria.

## Dependencies and boundaries

The Safety Plan connects to Task Management, equipment, workforce and competence, SRB, PTW, LOTO, PPE, operations/passdown, materials, ACOS and records/audit. Detailed PTW, LOTO and SRB rules are governed separately; this feature must not assume digital approval alone is equivalent to verified physical safety.

This PRD does not prescribe a technology stack, risk formula, exact legal applicability, equipment safety procedures or production-release authorization.

## Open decisions and principal risks

Before approval, decide the exact screening questions and hazard catalogue; risk methodology and thresholds; SRB, permit and isolation relationships; permissions and independent approvals; change/revision policy; records and retention; and the authority for reusable form publication.

The largest risks are an unapproved hazard mapping, conflicting approval or permit rules, silently lost conditional answers, stale safety decisions, and an interface implying controls are physically verified when they are not.

See the single [Decision Register](02-decision-register.md) and [Historical Source Reconciliation](03-source-reconciliation.md).

## Acceptance and governance

Acceptance requires product, technical and safety review; source-traced decisions; verified user journeys and negative scenarios; and an approved baseline. Implementation progress is not equivalent to safety authorization.

Related GitHub issues: [FP-014](https://github.com/sagrado26/FabOps-Green/issues/14), [FP-015](https://github.com/sagrado26/FabOps-Green/issues/15), [FP-016](https://github.com/sagrado26/FabOps-Green/issues/16), [FP-017](https://github.com/sagrado26/FabOps-Green/issues/17).

## Change history

| Version | Date | Change |
|---|---|---|
| 0.5 | 2026-10-14 | Executive summary established alongside the detailed Technical PRD; no approval claimed |
