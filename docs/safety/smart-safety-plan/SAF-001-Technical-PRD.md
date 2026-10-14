# SAF-001 — Smart Safety Plan
## Product Requirements Document | Technical v0

| Document control | |
|---|---|
| Product / function | FabPilot / Safety |
| Feature | SAF-001 |
| Version | v0 (initial baseline proposal) |
| Status | Draft — subject to product, technical and safety review |
| Product counterpart | [Executive PRD v0](SAF-001-Executive-PRD.md) |
| Decisions | [Decision Register](02-decision-register.md) |

## 1. Scope and interpretation

This document translates the [Executive PRD](SAF-001-Executive-PRD.md) into testable functional behaviour and data needs. It specifies outcomes and safety boundaries without requiring a specific framework, API, or database.

**Requirement states:** Requirements are proposed, not yet approved. `TBD` identifies a decision needed before implementation or release. Compliance and physical-control verification must be established by applicable authorities.

## 2. Four-stage functional contract

### Stage 1 — Task Details

The form is associated with one task and relevant asset context. The user sees available task identity, equipment, planned scope, work location, responsible person, participation and relevant work conditions. Missing, changed or ambiguous context is clearly identified. Trusted data may be prefilled, but users must not silently alter authoritative task records through a plan field.

### Stage 2 — Hazard Identification

Present the intended twelve pre-task screening questions from a controlled, versioned source once approved. Answers distinguish Yes, No and unanswered. Relevant answers reveal selectable hazard(s), events, outcomes and concise guidance. An engineer can identify task-specific hazards not covered by the baseline; such additions require documented review policy.

Visibility must not erase prior answers. Hidden answers and explicitly cleared answers are different user actions and must be handled consistently. Missing or unknown catalogue information must not generate fictitious hazard data.

### Stage 3 — Risk Assessment

Carry selected hazard identifiers and relevant context into the assessment. Capture initial risk, controls, additional mitigations, residual risk, responsible persons and evidence where required. Risk calculations and acceptability levels come from one approved methodology; the form must not define a competing formula.

Linked PTW, isolation, PPE or competence requirements remain independently governed. A recommended or selected control is not the same as verified implementation.

### Stage 4 — Review & Approval

Summarize assessed work, hazard answers, risks, proposed controls, unresolved conditions, required linked obligations and current revision. Eligible reviewers may accept, reject or request change in accordance with an approved authorization matrix. A decision records its actor, reason as applicable, time and applicable revision.

Readiness should distinguish informational notices from conditions that prevent permitted start/restart. The exact transition-specific rules need approval.

## 3. Detailed requirement register

| ID | Outcome / required behaviour | Capability |
|---|---|---|
| SAF-REQ-001 | Create a Safety Plan linked to a real task and equipment/work context | 01 |
| SAF-REQ-002 | Save and reopen incomplete drafts without loss | 02 |
| SAF-REQ-003 | Guide users through four coherent stages | 02 |
| SAF-REQ-004 | Present the approved screening questions and distinguish unanswered answers | 03 |
| SAF-REQ-005 | Reveal relevant hazard choices and guidance for applicable responses | 03, 04 |
| SAF-REQ-006 | Allow appropriate addition of task-specific hazards with provenance | 03 |
| SAF-REQ-007 | Carry selected hazards and mapped context into assessment without duplicate entry | 03, 05 |
| SAF-REQ-008 | Capture initial/residual risk and mitigations using a governed method | 05 |
| SAF-REQ-009 | Indicate applicable safety obligations and their verification status | 06 |
| SAF-REQ-010 | Refuse incomplete or invalid submission and review actions | 07 |
| SAF-REQ-011 | Permit review/approval/rejection only by authorized people with auditable decisions | 07 |
| SAF-REQ-012 | Provide current readiness and enforce binding start-work prerequisites | 08 |
| SAF-REQ-013 | Reassess relevant plan impacts when work conditions change | 09 |
| SAF-REQ-014 | Preserve approved historical revisions and decisions | 10 |
| SAF-REQ-015 | Avoid inconsistent or misleading outcomes after conflicting edits or failures | 10 |
| SAF-REQ-016 | Support accessible keyboard, touch, desktop and mobile use | 02 |
| SAF-REQ-017 | Support participant awareness and handover obligations | 11 |
| SAF-REQ-018 | Reuse approved templates without rewriting previous plans | 12 |
| SAF-REQ-019 | Send governed change signals to operational coordination | 13 |
| SAF-REQ-020 | Display relevant safety status and controls inside the Task Workspace | 13 |
| SAF-REQ-021 | Source active question definitions from governed content, not arbitrary presentation data | 03, 12 |
| SAF-REQ-022 | Preserve saved answers when conditional inputs are hidden; govern explicit clearing separately | 02, 12 |
| SAF-REQ-023 | Allow incomplete drafts; require suitable completeness on submission | 02, 07 |
| SAF-REQ-024 | Handle conditional dependencies correctly, including chained and invalid conditions | 12 |
| SAF-REQ-025 | Ensure trusted authorization governs safety decisions; UI display alone cannot authorize work | 07, 08 |
| SAF-REQ-026 | Support controlled form configuration, preview, publishing and versioned use | 12 |
| SAF-REQ-027 | Detect stale or conflicting changes before accepting and representing them as saved | 09, 10 |
| SAF-REQ-028 | Preserve provenance of the questions, risk method and controls used for a decision | 10, 12 |
| SAF-REQ-029 | Define SRB reassessment separately from ordinary plan revision, subject to approved policy | 07, 09 |
| SAF-REQ-030 | Govern PTW, LOTO, acknowledgments and competence requirements by task transition | 06, 08 |
| SAF-REQ-031 | Use appropriate, consistent and source-verified hazard symbols | 04 |
| SAF-REQ-032 | Maintain one canonical plan creation, editing and review journey | 01, 13 |

## 4. Field groups (functional, not database schema)

| Stage | Core information | Conditional information |
|---|---|---|
| Details | Task ID, asset, scope, responsible person | Location, planned period, equipment condition, related work, participants |
| Hazards | Question and answer, selected hazard, controlled source version | Additional hazards, notes, mapped events/consequences, evidence |
| Risk | Hazard, initial/residual evaluation, planned controls | Control verification, owner, linked permits/isolation/PPE, escalation |
| Review | Current revision, summary, outstanding items, decision status | Reviewer rationale, acknowledgment, evidence and readiness blockers |

The exact mandatory/optional fields, types, defaults and conditional mappings are **TBD** pending governed catalogue and workflow decisions.

## 5. Lifecycle and error behaviour

| Event | Expected behaviour |
|---|---|
| Create | Establish task association and save a draft |
| Resume | Restore entered values and relevant context |
| Submit | Validate current required information before review |
| Review | Apply authorized decisions to the correct plan revision |
| Revise | Preserve earlier decisions and reassess the impact of changes |
| Start/restart request | Recheck current binding prerequisites; show unresolved actions |
| Participant / shift change | Carry forward applicable safety context and any governed acknowledgment |
| Concurrent update or failure | Reject or resolve conflict safely without false success or partial authorization |

Specific state names, expiry and reopen paths are **TBD**. Work task lifecycle and safety plan lifecycle must not be conflated.

## 6. Integration and record contract

Each plan needs an identifiable task, revision, actor and time for relevant events. The historical record needs the assessed facts, hazard catalogue/risk-method versions, mitigation and control status, reviewer decisions and evidence links. Changes to shared data must not silently rewrite approved historical meaning.

The solution must distinguish authoritative facts from informational copies. PTW, LOTO, SRB and workforce approvals retain their own authority and interfaces. ACOS may respond to recorded events but must not grant unapproved safety permissions.

## 7. Verification criteria

Verification must cover the four-stage happy path and at least: incomplete submission, unknown hazard mapping, conditional answer hide/show, explicit clearing, stale revision, unauthorized review, missing permit/isolation prerequisites, changed task scope, mid-work reassessment, multi-shift handover, concurrent decisions and loss of external service.

For each `SAF-REQ`, final acceptance evidence must identify a test, reviewer and result. Tests for physical-control verification require qualified operational review; an automated UI test is insufficient.

## 8. Outstanding decisions and completion gate

The [Decision Register](02-decision-register.md) remains authoritative for unresolved design and safety decisions, including the exact twelve questions, risk thresholds, SRB relationships, PTW/LOTO transition rules, approval roles, records policy and content publication rights.

**Ready for implementation** only after affected requirements and acceptance criteria are reviewed and authorized. **Ready for operational use** only after applicable safety governance, validation and deployment checks are approved.


**User workflows and swimlanes:** [SAF-001 User Workflows](SAF-001-User-Workflows.md) — plan creation, review, readiness, handover and controlled template publication.

## 9. Participant acknowledgment — core v0 functional requirements

**Applies to:** SAF-REQ-017 (participant awareness and handover) and SAF-REQ-030 (transition-sensitive requirements). This section refines, rather than replaces, those IDs. Individual acknowledgment is neither Safety Plan approval nor physical-control verification.

| Rule ID | Proposed business rule | Evidence / acceptance |
|---|---|---|
| BR-058 | Individually identify engineers named on the applicable Safety Plan. | Unique participant records and role snapshot |
| BR-059 | Provide named engineers access to the applicable revision before acknowledgment. | Role/access check and revision shown |
| BR-060 | Record acknowledgment by actor, plan revision and timestamp. | Auditable acknowledgment record |
| BR-061 | Disallow acknowledging on behalf of another person unless a separately approved delegation procedure exists. | Identity and impersonation rejection tests |
| BR-062 | Require newly named participants to review and acknowledge according to approved participation policy. | Add-participant journey and policy outcome |
| BR-063 | Trigger renewed acknowledgment for material revisions where the approved policy requires it. | Revision impact tests |
| BR-064 | Surface pending acknowledgments to Action Lead and relevant participants. | Task and Safety Plan UI state tests |
| BR-065 | Keep acknowledgment separate from approval, toolbox-talk attendance and start-work authorization. | Four distinct records and permission tests |

**Candidate policy, not approved:** The Action Lead acknowledges; a one-person task may satisfy its acknowledgment requirement with the Action Lead alone. Other named engineers add personal acknowledgments. Do not automatically stop or re-gate work already in progress simply on acknowledgment changes. The definitive start/restart gate, acknowledgment minimum, participant removals and escalation rules require Safety Authority authorization.

**Acceptance scenarios:** solo engineer; lead plus participants; late joiner; unacknowledged participant; rejected/withdrawn acknowledgment; material revision; handover; already-running task; unauthorized on-behalf-of action; stale acknowledgment against a superseded revision.

## 10. Confirmed product directions and implementation boundaries

SAF-DEC-001: Twelve controlled pre-task questions form the initial baseline; publish authorized versioned changes only. No unapproved catalogue entries are invented.

SAF-DEC-002: The selected product model uses severity 1–3, likelihood 1–4, computed index = severity × likelihood, maximum individual-risk roll-up and SRB trigger at ≥6. Do not equate this product selection with approved site risk acceptance or override independent controls.

SAF-DEC-003: Apply global governed standards plus applicable, authorized local/site/customer/equipment requirements; track the chosen provision and version per assessment.

SAF-DEC-004: SRB, PTW and LOTO remain independent governed workflows; the Safety Plan references obligations and authoritative statuses. No generic auto-close or hard-stop-on-expiry is inferred.

SAF-DEC-005: Eligible personnel may prepare/submit; governed approval follows an explicit matrix. Action Lead acknowledgment and each named engineer acknowledgment are distinct events from approval, toolbox talk and work permission.

SAF-DEC-006: The Action Lead records a reassessment decision with a reason, but mandatory escalation triggers override discretionary decisions. Exact triggers require approval.

SAF-DEC-007: Maintain standard attributable revision, approval/rejection and acknowledgment history with role-based access. Any legal retention/record integrity obligation still applies; enhanced legal-hold/signature products are not first-release commitments.

SAF-DEC-008: Software release acceptance requires functional testing and Product Owner acceptance. Site/EHS compliance and safety authorization remain separate non-waivable obligations where applicable. A mandatory site pilot is not part of the selected standard release model.

See the [single decision register](02-decision-register.md) for outstanding choices and approval evidence.
