# SAF-001 — Smart Safety Plan
## Product Requirements Document | Executive v0

| Document control | |
|---|---|
| Product | FabPilot |
| Function | Safety |
| Feature | SAF-001 — Smart Safety Plan |
| Version | v0 (initial baseline proposal) |
| Status | Draft — pending product and safety approval |
| Owner | Product Owner (to assign) |
| Reviewers | Safety, Operations, Engineering (to assign) |
| Detailed companion | [Technical PRD v0](SAF-001-Technical-PRD.md) |

## 1. Product purpose

FabPilot Smart Safety Plan enables engineers to prepare, assess, review, and maintain task-specific safety planning within the maintenance workflow. It connects work scope, hazard identification, risk assessment, required controls and authorized review in one coherent experience.

The plan helps people make informed decisions; it does not itself establish that physical controls have been applied.

## 2. Problem and outcomes

Maintenance tasks involve equipment hazards, changing work conditions, multiple participants and safety obligations. Separate forms and disconnected status updates can cause duplicated entry, lost context and uncertainty about current requirements.

The product should:
- reduce avoidable administrative entry without reducing assessment quality;
- provide relevant hazard and control guidance when the engineer needs it;
- make incomplete actions and safety-related blockers understandable;
- support reviews and revisions when work changes;
- keep an intelligible history for subsequent shifts and audits.

## 3. Users

| User | Primary need |
|---|---|
| Field Service Engineer | Prepare and update the task Safety Plan |
| Task Lead | Coordinate team awareness and task readiness |
| Reviewer / authorized approver | Assess the submitted plan and record a decision |
| Participating engineer | Understand hazards and obligations relevant to the assigned work |
| Operations | View planning status and outstanding requirements |
| Safety content administrator | Maintain controlled screening and hazard content |

Role permissions and approval authority will be established in the supporting governance specification.

## 4. Product scope

**Included:** one task-linked Safety Plan; draft and resume; hazard screening; selection of applicable hazards; initial and residual risk with task-specific controls; review and authorization; revisions; relevant readiness indications; participation/shift awareness; traceable records; connections to PTW, LOTO, SRB, PPE, Task Management and Materials when applicable.

**Outside this feature:** the independent administration of permits, physical isolation, equipment safeguards, training systems and enterprise-wide standards governance. The Safety Plan may depend on their statuses but does not replace those processes.

## 5. Four-stage experience

| Stage | User objective | Expected product experience |
|---|---|---|
| 1. Task Details | Confirm the work being planned | Relevant task, asset, people and work conditions appear with minimal re-entry |
| 2. Hazard Identification | Identify applicable hazards | A compact screening form with the intended twelve pre-task questions; relevant answers reveal hazard choices and supporting guidance |
| 3. Risk Assessment | Evaluate and mitigate risks | Selected hazards carry forward into an assessment of unwanted events, consequences, controls and residual risk |
| 4. Review & Approval | Confirm completeness and obtain an authorized decision | The plan summary identifies unresolved items, linked safety requirements, review results and readiness implications |

The exact twelve question texts, mappings and risk method must be controlled and approved before a live safety process relies on them.

## 6. Product capabilities

| ID | Capability | User outcome |
|---|---|---|
| SAF-CAP-01 | Task context | A plan reflects the correct task and equipment |
| SAF-CAP-02 | Draft management | Work can be paused and resumed without re-entry |
| SAF-CAP-03 | Hazard identification | Relevant hazards can be identified consistently |
| SAF-CAP-04 | Hazard guidance | Users understand likely events, outcomes and baseline controls |
| SAF-CAP-05 | Risk assessment | Risks and proposed mitigations can be evaluated consistently |
| SAF-CAP-06 | Safety obligations | Required PTW, LOTO, PPE and competency actions are visible |
| SAF-CAP-07 | Review and approval | Decisions come from authorized reviewers and remain traceable |
| SAF-CAP-08 | Readiness | Users understand whether further safety action is required before work |
| SAF-CAP-09 | Reassessment | Relevant changes prompt appropriate review of the plan |
| SAF-CAP-10 | Records | Past versions and decisions remain retrievable |
| SAF-CAP-11 | Participation and passdown | Current safety information follows people and shifts |
| SAF-CAP-12 | Controlled content | Approved templates and hazard content can be maintained |
| SAF-CAP-13 | Connected operations | The plan appears naturally in the Task Workspace and can support governed ACOS coordination |

## 7. Experience principles

Safety before productivity; concise screens; progressive disclosure; one clear primary action; prominent unfinished safety obligations; accessible responsive layout; no duplicated assessment or approval path. Use the FabPilot primary colour `#0F238C` for ordinary interface styling while preserving distinct semantic safety states.

## 8. Dependencies

The plan depends on Task Management for task context, Equipment for asset context, Workforce for user eligibility, Safety subsystems for their independently verified obligations, Operations for handover, Materials for material-related hazards, and Platform/ACOS for records and change awareness.

## 9. Success measures

Measure preparation effort, completion quality, outstanding-control visibility, review turnaround, revisions after changed conditions, handover continuity and traceability. Targets and collection methods are set during business-case review; speed alone is not a safety-performance measure.

## 10. Acceptance and decisions

The v0 product baseline is accepted only when the Product Owner and designated safety authority approve the scope, the four-stage journey, key capabilities, and the boundaries between planning, approval and physical verification.

Open matters: definitive screening catalogue; risk methodology; approval/acknowledgment responsibilities; when changes require reassessment; linked PTW/LOTO/SRB rules; retained records and site-specific obligations. Track outcomes in the [Decision Register](02-decision-register.md).

**Detailed requirements and acceptance scenarios:** [Technical PRD v0](SAF-001-Technical-PRD.md). Neither document independently authorizes equipment maintenance.


**User workflows and swimlanes:** [SAF-001 User Workflows](SAF-001-User-Workflows.md) — plan creation, review, readiness, handover and controlled template publication.

## Safety Plan acknowledgment — core v0 capability

Every named participant needs access to the applicable Safety Plan and an attributable way to confirm review and understanding. The **Action Lead acknowledgment** and **named engineer acknowledgments** are recorded separately from Safety Plan approval, toolbox-talk attendance, and permission to start work.

A single-person task is supported. Whether acknowledgments from every named participant are prerequisites to initial Start Work, and whether an already-running task is re-gated, remain explicit Safety Authority decisions. Historic FabPilot rulings are candidates, not automatically adopted into FabOps-Green. Outstanding acknowledgments are visible during preparation and shift handover.

**Traceability:** SAF-REQ-017, SAF-REQ-030; business rules BR-058–BR-065; [acknowledgment workflow](SAF-001-User-Workflows.md).
