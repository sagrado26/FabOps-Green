# SAF-001 — Requirements Review v0

**Review date:** 2026-10-14  
**Review type:** Independent document quality and consistency review  
**Scope:** Current SAF-001 documentation on `docs/saf-001-product-requirements` in FabOps-Green  
**Disposition:** CHANGES REQUIRED — not approved for development baseline or operational use  
**Review authority:** Document analysis only; product, safety, legal and engineering sign-off remains pending.

## Executive finding

The product objective, task-linked four-stage workflow and high-level feature outcomes are sufficiently coherent to inform design. The package is **not complete enough for controlled implementation or safety approval**. Major gaps involve authoritative hazard/risk content, transition-specific safety rules, process-rule traceability, acceptance tests and appointed reviewers.

## Review matrix

| Dimension | Assessment |
|---|---|
| Purpose, scope, user journeys | Adequate conceptual v0; product-owner sign-off pending |
| Four-stage UX | Adequate at outcome level; field/conditional specifics pending |
| User roles, competence, decision authority | Partial |
| Hazard questions and mapping | Blocking: authoritative twelve-question catalogue absent |
| Risk methodology and thresholds | Blocking: not approved |
| SRB, PTW, LOTO and task transition policy | Blocking: approvals and actual work rules unresolved |
| Engineer acknowledgment | Documented in BR-058–065; exact gate policy unresolved |
| Business rule registry / traceability | High gap: original BR-001–057 not incorporated as individually controlled entries |
| Data model, interfaces, privacy and records | Preliminary logical coverage; no approved contracts |
| Acceptance scenarios | Twelve broad cases; insufficient requirement-level evidence |
| Standards/legal applicability | Candidate register only |
| Accountable review and sign-off | Unassigned |

## Numbered findings and corrective actions

| ID | Severity | Finding | Required correction | Suggested owner | Closure evidence |
|---|---|---|---|---|---|
| REV-001 | High | BR-001–057 are absent as a full controlled catalogue from Process & Business Rules. | Restore each unique rule, remove duplicate authority, map to SAF-REQ and states/decisions. | Product + Safety | Complete rule-to-requirement matrix |
| REV-002 | Blocker | Twelve exact screening questions, mapping sources and active applicability remain unknown. | Supply/approve versioned catalogue and handling of No, Yes, unknown and conditional dependency. | Safety content owner | Approved catalogue and mapping checks |
| REV-003 | Blocker | Initial/residual methodology, thresholds and risk acceptance undefined. | Adopt one approved method, escalation matrix and residual-risk authority. | Safety authority | Signed method plus test vectors |
| REV-004 | Blocker | SRB/PTW/LOTO/start-work interactions remain unresolved, including active-work treatment. | Approve per-transition decision table; distinguish safety planning and independent physical authorization. | Safety + Operations | Transition matrix and negative-path scenarios |
| REV-005 | High | Engineer acknowledgment defined but minimum/gating unresolved. | Decide lead/other acknowledgments, solo work, late joiner, revision, shift transfer and in-progress effect. | Safety + Operations | Signed participation rule set |
| REV-006 | High | Verification has twelve broad cases, not direct evidence for all 32 requirements and 65 business-rule IDs. | Define scenario IDs, inputs, expected outcomes, responsible reviewer, test layer and links per requirement. | QA + Safety | Coverage matrix and acceptance cases |
| REV-007 | High | Product/safety/engineering/records approval owners unspecified. | Appoint accountable owners and define disposition control. | Product Owner | Governance/RACI and recorded approvals |
| REV-008 | Blocker for operational release | Applicable legal/site/equipment obligations are not established. | Record relevant precise provisions, context, status and documented reviewer rationale. | EHS/Legal | Approved applicability register |
| REV-009 | High | Records integrity, retention, recovery and audit evidence not specified at verifiable level. | Specify applicable retention, signed actor identity, recovery objectives and history rules. | Security + Records | Approved control and test requirements |
| REV-010 | High | Original external ISP specification not fully compared with baseline. | Compare original exact source where available, capture accepted, rejected and deferred source requirements. | Product + Safety | Reconciled source-decision matrix |

## Consistency corrections

1. Treat all newly written v0 documents as draft proposals; inherited FabPilot rulings remain reference inputs until explicitly adopted.
2. The Executive PRD may summarize capabilities while the Technical PRD owns the 32 detailed SAF-REQ IDs.
3. The controlled Process & Business Rules register should own BR-001–065, referring to the separate acknowledgment detail without conflicting duplicate wording.
4. Distinguish plan approval, SRB outcome, engineer acknowledgment, toolbox talk, permit/isolation verification and start-work authorization as separate events and evidence.
5. Resolve two priority questions: whether acknowledgment is an initial-start gate and whether any status change during already-running work triggers a new gate.
6. Ensure each cross-document link points to the exact active specification and approved decision, not solely a historical candidate.

## Prioritized resolution sequence

**Gate A — Requirement integrity:** Close REV-001, establish source links and requirement coverage; close any missing user stories.

**Gate B — Safety content:** Close REV-002, REV-003, REV-004 and REV-005 with accountable EHS/operations decisions.

**Gate C — Delivery assurance:** Close REV-006, REV-007 and REV-009 with review ownership, verifiable tests and records controls.

**Gate D — Formal baseline:** Close REV-008 and REV-010 as relevant; record product, safety and technical review, and only then authorize the approved specification.

## Review conclusion

**Not approved.** The documentation package is a coherent working v0 draft. The review found ten corrective actions; four have blocking consequences for either the implementation baseline or operational release. The status cannot advance to *Baselined* solely by closing this review file. Actual product and safety authority decisions and evidence are required.
