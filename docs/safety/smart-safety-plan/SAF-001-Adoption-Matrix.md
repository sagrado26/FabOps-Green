# SAF-001 — FabPilot to FabOps-Green Adoption Matrix (v0)

**Status:** Draft for controlled adoption review · **Prepared:** 2026-10-14  
**Scope:** Historical FabPilot decisions as candidate inputs for the new SAF-001 baseline.  
**Authorization boundary:** Approval to *prepare this matrix* is **not** an adoption of individual risk, permit, isolation, approval or work-permission rules. Each disposition below remains proposed until an accountable authority explicitly signs its decision.

See [Executive PRD](SAF-001-Executive-PRD.md), [Technical PRD](SAF-001-Technical-PRD.md), [Requirements Review](SAF-001-Requirements-Review-v0.md) and [Decision Register](02-decision-register.md).

## Disposition codes

- **Proposed adoption:** historical rule is a plausible product baseline but needs local sign-off.
- **Reconcile:** historical sources/implementation status or external ISP policy differ; cannot adopt without resolving.
- **Evidence gap:** source is insufficient for a binding requirement or release.
- **Deferred:** not a decision for the SAF-001 v0 baseline.

## Candidate source decisions

| ID | Historical evidence | Decision or limitation to evaluate | FabOps-Green disposition | SAF-REQ | Review / acceptance gate |
|---|---|---|---|---|---|
| ADOPT-01 | [ADR-0026](https://github.com/sagrado26/fabpilot-fsm/blob/main/Documentation/decisions/0026-safety-index-scoring.md) | Severity 1–3 × likelihood 1–4; system-computed index; banding and SRB trigger ≥6. The “high = 5” band is mathematically unreachable. | **Proposed adoption** | 008, 028 | Safety Authority signs risk scales, labels, thresholds, tests. REV-003 |
| ADOPT-02 | [ADR-0033](https://github.com/sagrado26/fabpilot-fsm/blob/main/Documentation/decisions/0033-per-risk-scoring-and-assessment-ownership.md) | Each risk scored separately; highest risk rolls up; empty or incomplete risks cannot count as low; risk revisions and plan ownership. Historical ADR acknowledges unresolved implementation aspects. | **Reconcile** | 007–008, 013–015, 028 | Approve revision/roll-up and regression scenarios. REV-003, REV-006 |
| ADOPT-03 | [ADR-0027](https://github.com/sagrado26/fabpilot-fsm/blob/main/Documentation/decisions/0027-safety-review-board-escalation-and-sign-off.md) | Triggered SRB uses multi-party review, Action Lead acknowledgment, mandatory EHS and an operational approver; later amendments qualify version and reassessment behavior. | **Reconcile** | 009–012, 025, 029–030 | Review current amendments and external process; sign transition matrix. REV-004 |
| ADOPT-04 | [ADR-0040](https://github.com/sagrado26/fabpilot-fsm/blob/main/Documentation/decisions/0040-submission-independence-prefill-and-acknowledgement.md) | Plan submission independent of isolation ownership; new-shift plan carries approved assessment context but not participants; submitted plan and SRB acknowledgments follow separate rules. | **Proposed adoption, subject to scope** | 010–011, 017, 025, 029–030 | Approve role/participation and submission gates. REV-004, REV-005 |
| ADOPT-05 | [4 Oct owner rulings](references/legacy-srb-ptw-owner-rulings-2026-10-04.md) | Action Lead acknowledgment mandatory; solo tasks possible; named personnel add acknowledgments; existing in-progress tasks not automatically re-gated. | **Proposed adoption** | 017, 030 | Explicit decision for solo, late joiner, new revision, restart/in-progress; test BR-058–065. REV-005 |
| ADOPT-06 | [ADR-0040 amendments](https://github.com/sagrado26/fabpilot-fsm/blob/main/Documentation/decisions/0040-submission-independence-prefill-and-acknowledgement.md) and [owner rulings](references/legacy-srb-ptw-owner-rulings-2026-10-04.md) | PTW requires type/duration and authority; permit expiry during active work described as notice-only in historic ruling; terminal plan outcomes can void permits. | **Reconcile; safety-critical** | 009, 012, 025, 030 | Decide individual start/restart/continuation/close effects; no default blanket stop or approval. REV-004 |
| ADOPT-07 | [ADR-0040 Amendment 2](https://github.com/sagrado26/fabpilot-fsm/blob/main/Documentation/decisions/0040-submission-independence-prefill-and-acknowledgement.md) | Lockbox/isolation custody is a parallel system; transfer should not automatically approve/close plan; competency required for custody. | **Proposed adoption** | 009, 012–013, 025, 030 | Approve independent verification, transfer and restoration. REV-004 |
| ADOPT-08 | [ADR-0030](https://github.com/sagrado26/fabpilot-fsm/blob/main/Documentation/decisions/0030-append-only-record-correction.md) | Governed revisions instead of edits to approved decisions; corrections append errata, not mutate safety authority. ADR describes implementation eligibility gaps. | **Proposed adoption with gap review** | 014–015, 027–028 | Approve record integrity/correction controls and tests. REV-009 |
| ADOPT-09 | [Data governance](https://github.com/sagrado26/fabpilot-fsm/blob/main/Documentation/remediation/pre-redesign/DATA-GOVERNANCE.md) | Retain historical evidence pending a defined schedule; no invented legal period; restrict confidential data and actor identity. | **Proposed adoption, legal retention unresolved** | 014–015, 028 | Privacy/records owner sets lawful schedule, access, backup/deletion and hold rules. REV-008–009 |
| ADOPT-10 | [Pre-task reconciliation](references/legacy-isp-reconciliation-2026-10-04.md), [Technical PRD](SAF-001-Technical-PRD.md) | Intended 12 questions, hazard/event/control mapping and governed form conditions; exact controlled catalogue not established. | **Evidence gap** | 004–007, 021–024, 026, 031 | Approved 12-question wording and mappings required. REV-002 |
| ADOPT-11 | [FabPilot historical reconciliation](references/legacy-isp-reconciliation-2026-10-04.md) | Historical external ISP specification reviewed, but full original source not reconciled in new baseline. | **Evidence gap** | 001–032 | Obtain/reconcile authoritative original and disposition each discrepancy. REV-010 |
| ADOPT-12 | [Requirements Review](SAF-001-Requirements-Review-v0.md) and current v0 docs | 32 SAF requirements; BR-058–065 documented; BR-001–057 not fully carried into controlled rule register. | **Evidence gap** | 001–032 | Establish full rule inventory and test links, owners and sign-off. REV-001, REV-006–007 |

## Adoption / decision record

For each ADOPT item, record **approved disposition**, precise source revision, accepted rule wording, exceptions, impacted requirement IDs, responsible Safety/Product/Technical authority, date, test evidence and approver. Do not infer authorization from an accepted *legacy* ADR.

| ID | Decision owner | Decision | Approval date | Evidence |
|---|---|---|---|---|
| ADOPT-01–12 | To be assigned per item | **Pending** | — | — |

## Completion gate

- [ ] Assign owners and resolve source authority
- [ ] Approve controlled question/hazard catalogue and risk methodology
- [ ] Resolve SRB, PTW, LOTO and all transition-specific permissions
- [ ] Decide acknowledgment requirements and exceptions
- [ ] Complete BR → SAF-REQ → test traceability
- [ ] Confirm applicable standards and privacy/retention duties
- [ ] Obtain independent product, safety and technical approval

**Disposition:** Matrix prepared; no individual safety rule is approved by this file. Documentation PR remains draft and no application code is changed.

## Reconciliation with confirmed SAF-DEC-001–008

The Product Owner has confirmed the eight decisions in the [Decision Register](02-decision-register.md). Corresponding historical models are now **selected product direction**, not automatically adopted operational safety rules. Individual ADOPT-01–12 dispositions remain pending source validation and relevant EHS/site/legal authority. Do not interpret standard software release as a waiver of required safety approval, or automatically change live permit/isolation behavior.
