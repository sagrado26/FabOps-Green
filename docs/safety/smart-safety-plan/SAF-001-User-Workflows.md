# SAF-001 — User Workflows and Swimlanes (v0)

**Status:** Draft — for product, operations and safety review.  
**Companion:** [Executive PRD](SAF-001-Executive-PRD.md) · [Technical PRD](SAF-001-Technical-PRD.md) · [Decision Register](02-decision-register.md)

These diagrams express **proposed user journeys**, not an approved authorization policy. A system readiness notice is not proof of physical isolation or permission to work. Exact approver, acknowledgment, SRB, PTW and LOTO rules remain decisions to confirm.

## 1. End-to-end user journey

```mermaid
flowchart LR
  A["Open maintenance task"] --> B["Create or resume Safety Plan"]
  B --> C["1. Task Details"]
  C --> D["2. Hazard Identification"]
  D --> E["3. Risk Assessment and controls"]
  E --> F["4. Review and submit"]
  F --> G{"Review outcome"}
  G -->|Changes requested| C
  G -->|Approved| H["Check current linked requirements"]
  H --> I{"Start-work prerequisites satisfied?"}
  I -->|No| J["Display outstanding actions"]
  J --> H
  I -->|Yes| K["Task execution may proceed under applicable authority"]
  K --> L{"Relevant work conditions changed?"}
  L -->|Yes| M["Reassess impacts and apply required review"]
  M --> H
  L -->|No| N["Record task completion and retain history"]
```

## 2. Swimlane — plan preparation and review

```mermaid
sequenceDiagram
  autonumber
  participant E as Field Service Engineer
  participant S as Smart Safety Plan
  participant T as Task / Equipment
  participant R as Authorized Reviewer
  E->>S: Create or resume plan for task
  S->>T: Obtain current task and equipment context
  T-->>S: Context, identity and version
  S-->>E: Stage 1: Task Details
  E->>S: Confirm task and work conditions
  S-->>E: Stage 2: Hazard Identification
  E->>S: Answer screening questions and select hazards
  S-->>E: Show mapped guidance and selected risks
  S-->>E: Stage 3: Risk Assessment
  E->>S: Enter evaluation, mitigations and control status
  E->>S: Stage 4: Review and submit
  S->>S: Validate required information and current context
  alt Incomplete or stale
    S-->>E: Explain missing information or conflicting change
  else Valid submission
    S->>R: Request authorized review of this revision
    alt Changes required or rejected
      R-->>S: Record decision and reason
      S-->>E: Return for correction / reassessment
    else Approved under applicable policy
      R-->>S: Record decision and applicable revision
      S-->>E: Display review result and outstanding obligations
    end
  end
```

## 3. Swimlane — readiness and work execution

```mermaid
sequenceDiagram
  autonumber
  participant E as Task Lead / Engineer
  participant T as Task Workspace
  participant S as Safety Plan
  participant C as Independent Controls
  participant G as Governed Authorization
  E->>T: Request Start Work or restart
  T->>S: Check current plan revision and decision
  S-->>T: Plan outcome and obligations
  T->>C: Request PTW, LOTO, PPE and competence states where relevant
  C-->>T: Verified / pending / unknown states
  T->>G: Evaluate permitted task transition
  alt Requirement unsatisfied or unverifiable
    G-->>T: Deny transition with reason
    T-->>E: Show outstanding actions and readiness notice
  else All applicable prerequisites accepted
    G-->>T: Permit transition
    T-->>E: Work execution available
  end
  Note over E,G: Exact start/restart and in-progress rules require approval; digital checks do not replace physical verification.
```

## 4. Swimlane — material change and shift handover

```mermaid
sequenceDiagram
  autonumber
  participant O as Operations / Task Lead
  participant S as Smart Safety Plan
  participant E as Assigned Engineer
  participant R as Reviewer
  participant P as Incoming Shift
  O->>S: Report scope, team, equipment or control change
  S->>S: Identify affected assessed facts and requirements
  S-->>E: Show reassessment actions
  E->>S: Update assessment and submit revision where required
  opt Policy requires renewed approval
    S->>R: Submit changed revision for review
    R-->>S: Record decision
  end
  O->>P: Transfer task status and outstanding safety obligations
  P->>S: Review current applicable plan
  opt Acknowledgment required by approved policy
    P->>S: Record acknowledgment
  end
  S-->>O: Updated handover / readiness information
  Note over O,P: Do not discard live isolation or permit context when work pauses, transfers or aborts.
```

## 5. Swimlane — governed question/template publication

```mermaid
sequenceDiagram
  autonumber
  participant A as Safety Content Steward
  participant B as Form Builder
  participant R as Authorized Publisher
  participant S as Smart Safety Plan
  A->>B: Propose question, hazard mapping or presentation change
  B-->>A: Preview version and conditional behaviour
  A->>R: Request review and publication
  alt Rejected
    R-->>A: Return with reason
  else Approved for publication
    R->>B: Publish controlled version
    B->>S: Make approved version available to new/revised plans under policy
    S->>S: Preserve previous plan and catalogue references
  end
```

## 6. Journey traceability

| Workflow | Primary participants | Related requirements | Decision still open |
|---|---|---|---|
| Create / screen / assess / review | Engineer, Task, Reviewer | SAF-REQ-001–011, 021–024, 027, 032 | Exact catalogue and review authority |
| Check start/restart | Task Lead, Plan, PTW/LOTO, authorization service | SAF-REQ-009–012, 025, 030 | Gate differences by task transition |
| Change and handover | Operations, Engineer, Reviewer, incoming shift | SAF-REQ-013–015, 017, 028–030 | Revision and acknowledgment policy |
| Form definition publication | Steward, publisher, plan | SAF-REQ-018, 021–024, 026, 028, 031 | Builder permissions and version migration |

## 7. Acceptance checkpoints

- Each handoff or decision identifies the actor, current plan revision and relevant task.
- Draft save and submission are different operations; drafts may be incomplete.
- The question set and guidance come from an approved catalogue; unanswered is not No.
- Screen visibility changes do not implicitly erase saved answers.
- Review and start-work permissions are verified by trusted policy, not inferred from the UI.
- Denied or unavailable actions show actionable reasons without recording false success.
- Superseded reviews and source definitions remain reconstructable.
- All exception branches receive corresponding acceptance scenarios.

**Review gate:** Approve these journeys only after the exact safety policy, role matrix, source questions, risk methodology and SRB/PTW/LOTO interaction rules are resolved.

## 8. Swimlane — participant Safety Plan acknowledgment (proposed)

```mermaid
sequenceDiagram
  autonumber
  participant L as Action Lead
  participant S as Smart Safety Plan
  participant E as Named Engineer
  participant G as Governed Readiness
  L->>S: Confirm named participants and applicable plan revision
  S-->>E: Make plan and identified hazards / controls available
  E->>S: Open and review applicable revision
  E->>S: Record own acknowledgment
  S->>S: Store actor, revision and timestamp
  S-->>L: Show acknowledgment status and outstanding people
  L->>S: Record Action Lead acknowledgment
  S->>G: Provide current acknowledgment evidence
  G->>G: Apply approved transition-specific policy
  alt Acknowledgments required for this transition missing
    G-->>L: Show pending acknowledgments / restriction
  else Requirement satisfied or not applicable
    G-->>L: Show acknowledgment condition satisfied
  end
  Note over L,G: Acknowledgment is separate from plan approval, toolbox talk and start-work authority.
```

**Decision to approve:** exact minimum for one-person and multi-person tasks, late participants, reacknowledgment on material revision, and treatment of already-running work. Historical one-person and in-progress rulings remain candidates, not automatically binding.

**Linked requirements:** SAF-REQ-017, SAF-REQ-030; BR-058–BR-065.
