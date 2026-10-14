# SAF-001 — Smart Safety Plan: Product Requirements

| Attribute | Value |
|---|---|
| Product | FabPilot / FabOps Green |
| Function | Safety |
| Feature | SAF-001 — Smart Safety Plan |
| Document | 01 — Product Requirements |
| Version | 0.1 |
| Status | Draft — not approved |
| Date | 2026-10-14 |
| Owner / approver | To be appointed |
| Related development issues | FP-014, FP-015, FP-016, FP-017 |
| Next documents | Standards, Process Rules, Hazard Catalogue, Data Model, Roles, UX, Verification, Integration, Safety Assurance |

> **Safety assurance boundary:** This document proposes digital workflow requirements. Approval in software must not be confused with confirmation that physical isolation, equipment safeguards, permits, or other safety controls are actually implemented. Applicable legal, company and equipment-specific obligations must be validated by qualified authorities before use.

## 1. Purpose and problem

FabPilot Smart Safety Plan provides a task-linked, version-controlled workflow for identifying hazards, assessing risk, selecting and checking controls, reviewing and approving planned work, and detecting changes that may require re-assessment. Safety is embedded in maintenance task execution rather than presented as an isolated administrative form.

### Intended outcomes
- Help field service engineers prepare safe maintenance work with minimal unnecessary form completion.
- Make critical hazards and controls visible where task decisions are made.
- Prevent digital start-work authorization when required assessments, controls, or approvals have not been satisfied.
- Provide a reliable, reconstructable record of what was assessed, by whom, against which revision, and when.
- Support safe handover and controlled re-assessment during long or multi-shift work.

### Boundaries
**In scope:** four-stage plan, draft/resume, task/equipment linkage, screening, risk assessment, conditional control obligations, review/approval, readiness inputs, revisions, audit trail and interaction with tasks/PTW/LOTO/competence.

**Out of scope for this document:** the detailed independent implementations of PTW, LOTO and SRB; definitive risk calculation formula; statutory compliance assertions; production deployment policy; engineering implementation stack. Each needs its own approved specification.

## 2. Users and permissions (roles provisional)

| Persona | Activities | Authority boundary |
|---|---|---|
| Field Service Engineer / plan creator | Create, revise, select hazards, assess, attach evidence | Cannot self-grant approvals not authorized by policy |
| Task lead / responsible engineer | Coordinate participants, verify task relevance, submit | Exact approval rights TBD |
| Safety reviewer / authorized approver | Review hazards, controls and residual risks; decide approval | Approval authority, competency and separation rules TBD |
| Operations / scheduler | View readiness and scheduling implications | Readiness visibility does not confer safety approval |
| Participating engineer / handover recipient | Review and acknowledge applicable plan and obligations | Acknowledgment distinct from approval |
| Administrator / catalogue steward | Manage permitted configurations and controlled templates | Must not rewrite historical approved records |

All state-changing permissions must be enforced server-side, not merely by disabled UI buttons.

## 3. User experience — four stages

1. **Task Details:** link to the task, equipment, work scope, relevant conditions, participants and planned operation. Reuse trusted task data wherever possible; avoid repeated entry.
2. **Hazard Identification:** present **12 pre-task screening questions**. A Yes response opens relevant selectable hazards and concise contextual guidance; No responses should remain compact. Acknowledge missing/unknown information rather than silently treating it as No.
3. **Risk Assessment:** transfer selected hazards automatically to assessment rows with mapped hazardous event, unwanted outcome, consequence and baseline controls. Capture task-specific mitigations and initial/residual risk according to one approved risk methodology.
4. **Review & Approval:** summarise hazards, outstanding controls, linked permits and isolation obligations, unresolved exceptions, reviewer decisions and readiness impact. Require authorisation appropriate to the task.

The application should show baseline safety guidance progressively within a question/hazard card or compact detail space, without overwhelming users or misrepresenting recommendations as verified controls.

## 4. Product requirements

Priority P0 means required for initial functional acceptance; P1 means later capability, subject to product owner approval.

| ID | Priority | Requirement | Acceptance evidence |
|---|---|---|---|
| SAF-REQ-001 | P0 | Create a new Safety Plan linked to one task and identified equipment/work context. | Persist/reopen with correct task and equipment |
| SAF-REQ-002 | P0 | Save incomplete drafts and resume without losing entered answers. | Interrupted-entry test |
| SAF-REQ-003 | P0 | Present four ordered stages with clear progress and outstanding obligations. | UI walkthrough and state tests |
| SAF-REQ-004 | P0 | Display all 12 controlled screening questions; record Yes, No and unanswered distinctly. | Question catalogue contract test |
| SAF-REQ-005 | P0 | Yes responses expose relevant hazard choices and concise baseline guidance, with conditional details. | Per-question interaction test |
| SAF-REQ-006 | P0 | Allow authorized addition of task-specific hazards without overwriting baseline catalogue items. | Added-hazard audit test |
| SAF-REQ-007 | P0 | Carry identified hazards, events, outcomes and baseline controls into Risk Assessment without duplicate manual entry. | Cross-stage data consistency test |
| SAF-REQ-008 | P0 | Capture initial/residual risk, mitigation and control verification using one governed calculation/classification model. | Approved methodology and risk calculation tests |
| SAF-REQ-009 | P0 | Derive applicable obligations (e.g. PTW, LOTO, PPE, competence) from controlled rules; present source and verification status. | Rule mapping and exception tests |
| SAF-REQ-010 | P0 | Prevent submission/approval when required inputs are incomplete, rejected or stale. | Negative-path permission and validation tests |
| SAF-REQ-011 | P0 | Implement role-authorized review, approval and rejection with actor, timestamp, reason and plan revision. | Server-side authorization tests |
| SAF-REQ-012 | P0 | Derive readiness from the latest authoritative requirements and control statuses; block unsafe Start Work transitions. | End-to-end start-work gate tests |
| SAF-REQ-013 | P0 | Trigger assessment of impacts when task conditions, hazards, controls, participants, isolation or relevant linked facts change. | Change-driven invalidation tests |
| SAF-REQ-014 | P0 | Preserve approved plan snapshots, decision history and superseded revisions. | Historical record reconstruction test |
| SAF-REQ-015 | P0 | Fail safely under partial writes, stale screens, retries, concurrency and unavailable integrations. | Recovery/idempotency/concurrency tests |
| SAF-REQ-016 | P0 | Make keyboard, focus, contrast, touch targets and responsive four-stage use accessible. | Accessibility and responsive tests |
| SAF-REQ-017 | P1 | Support participant acknowledgment, handover and revision awareness. | Multi-shift scenario test |
| SAF-REQ-018 | P1 | Reuse controlled templates without silently altering prior approved plans. | Template versioning test |
| SAF-REQ-019 | P1 | Publish governed events for ACOS coordination and notifications with auditable outcomes. | Event/idempotency integration test |
| SAF-REQ-020 | P0 | Make safety controls visible from the task execution workspace without forcing duplicate workflows. | Integrated task journey test |

## 5. Core rules — draft, subject to formal approval

- A missing answer is **not** equivalent to No.
- A mapped baseline control is **guidance/requirement**, not evidence that the control has been implemented.
- Safety Plan readiness is a *signal*, not an independent substitute for physical verification.
- Approvals apply to a specific plan revision and relevant linked facts; later material changes require governed reconsideration.
- Only authorised users may approve, override, revise or restore controlled safety states; override rules, if any, require their own safety governance.
- Rejected or stale approvals must not partially modify records.
- Work must not start from an unqualified, unresolved or outdated safety state.
- The source of authority for every mandatory obligation must be traceable.

## 6. Interfaces and dependencies

| Interface | Required relationship |
|---|---|
| Task Management | Task identity, state, scope, work execution and start-work gate |
| Equipment | Asset identification, work context, equipment-specific risks |
| PTW / LOTO / PPE | Linked obligations and independently verified control state |
| Workforce / Identity | Qualified participants, roles, approval authorization |
| Operations / Passdown | Safety revision/hold/acknowledgment continuity |
| Materials | Relevant hazardous materials and changes in material context |
| ACOS | Event notifications, reevaluation and decision evidence |
| Records / Audit | Append-only decision history and retrieval of historical context |

## 7. Measures and non-functional requirements

Candidate KPIs, to be defined with baselines and targets: time to prepare/approve a plan; hazard selection and control completion quality; proportion of plans reopened for material changes; overdue approval counts; blocked start-work attempts; mismatch/exception rates; user correction rate. Do not optimize completion speed at the expense of control effectiveness.

Requirements for responsiveness, availability, retention, recovery time, performance, localization and audit data classification are **TBD**, not silently assumed.

## 8. Open decisions — blocking before baseline approval

| Decision ID | Question | Proposed owner |
|---|---|---|
| SAF-DEC-001 | What are the exact 12 screening questions, applicability and hazard mappings? | Safety authority / product owner |
| SAF-DEC-002 | Which risk methodology, thresholds and residual-risk approval gates apply? | Safety authority |
| SAF-DEC-003 | Which SEMI, legal, customer, corporate and equipment-specific obligations actually apply? | Compliance / safety authority |
| SAF-DEC-004 | What is the SRB relationship to the Safety Plan and how do PTW/LOTO states gate work? | Safety / engineering |
| SAF-DEC-005 | Who may create, submit, approve, reject, reopen and override, with what separation of duty? | Product owner / safety authority |
| SAF-DEC-006 | What constitutes a material change requiring re-review and acknowledgment? | Safety / operations |
| SAF-DEC-007 | What data retention, signing/evidence and privacy rules apply? | Security / records governance |
| SAF-DEC-008 | What are release scope, test thresholds and approved operational deployment conditions? | Product / release authority |

## 9. Document approval and traceability

**Draft → Product review → Technical review → Safety review → Owner approval → Baselined.** Approval remains pending. Implementers must link each change to a SAF-REQ ID, tests and a recorded design decision where applicable. No implementation completion or compliance approval is implied by this draft.

### Next documentation artifacts
- 02 Standards & Legal Basis
- 03 Process & Business Rules
- 04 Hazard & Risk Catalogue (12 questions and mappings)
- 05 Data Model & Records
- 06 Roles & Governance
- 07 UX Functional Specification
- 08 Verification & Acceptance
- 09 System Integrations
- 10 Safety Assurance & Failure Behaviour
- 11 Security, Privacy & Audit
- 12 Lifecycle & Change Management
- 13 Operations & Recovery
- 14 Business Case & KPIs

## 10. Change log

| Version | Date | Change |
|---|---|---|
| 0.1 | 2026-10-14 | Initial controlled requirements draft, pending reviews |
