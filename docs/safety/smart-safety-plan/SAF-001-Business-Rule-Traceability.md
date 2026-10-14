# SAF-001 — Controlled Business Rules and Requirement Traceability v0

**Status:** Draft / not approved. **Source:** SAF-001 Process & Business Rules v0 discussion and the acknowledged BR-058–065 definitions currently in this repository. **Date:** 2026-10-14.

This is the **single consolidated rule inventory**. The Executive PRD describes business outcomes, the Technical PRD holds SAF-REQ definitions, and this file holds individually numbered business rules. Historical decisions are candidate inputs only; `02-decision-register.md` governs open questions. **None of these entries alone authorize safety operations.**

## Classifications and ownership

- **Product:** Product Owner, with operational user review.
- **Safety-governed:** Designated Safety Authority and relevant Operations owner must decide applicability and required restrictions.
- **System control:** Architecture/security owner specifies enforcement; Safety Authority reviews safety-impacting behaviour.

These are proposed owner *roles*, not assigned named approvers.

## Traceability register

| Rule ID | Process | Draft rule | Requirements | Classification | Approval status |
|---|---|---|---|---|---|
| BR-001 | Task details | Every Safety Plan is associated with an identifiable maintenance task. | SAF-REQ-001, SAF-REQ-032 | Product | Draft; policy approval pending where applicable |
| BR-002 | Task details | Use applicable task and equipment context. | SAF-REQ-001 | Product | Draft; policy approval pending where applicable |
| BR-003 | Task details | Authorized users can save incomplete drafts. | SAF-REQ-002, SAF-REQ-003, SAF-REQ-016, SAF-REQ-023 | Product | Draft; policy approval pending where applicable |
| BR-004 | Task details | Changes to assessed task facts are evaluated for safety significance. | SAF-REQ-013 | Safety-governed | Draft; policy approval pending where applicable |
| BR-005 | Task details | Changes do not silently overwrite approved historical assessments. | SAF-REQ-014, SAF-REQ-028 | System control | Draft; policy approval pending where applicable |
| BR-006 | Hazard identification | Use approved version-controlled screening question definitions. | SAF-REQ-004, SAF-REQ-018, SAF-REQ-021, SAF-REQ-026 | Safety-governed | Draft; policy approval pending where applicable |
| BR-007 | Hazard identification | Distinguish unanswered from negative responses. | SAF-REQ-004, SAF-REQ-023 | Product | Draft; policy approval pending where applicable |
| BR-008 | Hazard identification | Relevant answers expose appropriate hazards and approved guidance. | SAF-REQ-005, SAF-REQ-007, SAF-REQ-031 | Product | Draft; policy approval pending where applicable |
| BR-009 | Hazard identification | Support task-specific hazards under an approved review process. | SAF-REQ-006 | Safety-governed | Draft; policy approval pending where applicable |
| BR-010 | Hazard identification | Carry identified hazards into risk assessment. | SAF-REQ-007 | Product | Draft; policy approval pending where applicable |
| BR-011 | Hazard identification | Hiding conditional questions does not silently erase answers. | SAF-REQ-022, SAF-REQ-024 | System control | Draft; policy approval pending where applicable |
| BR-012 | Risk assessment | Every applicable hazard requiring assessment is assessed. | SAF-REQ-007, SAF-REQ-008 | Safety-governed | Draft; policy approval pending where applicable |
| BR-013 | Risk assessment | Use the approved initial and residual risk methodology. | SAF-REQ-008 | Safety-governed | Draft; policy approval pending where applicable |
| BR-014 | Risk assessment | Identify and trace required mitigations. | SAF-REQ-008, SAF-REQ-009 | Safety-governed | Draft; policy approval pending where applicable |
| BR-015 | Risk assessment | Distinguish required controls from verified implementation. | SAF-REQ-009, SAF-REQ-025 | Safety-governed | Draft; policy approval pending where applicable |
| BR-016 | Risk assessment | Escalate risks under approved threshold rules. | SAF-REQ-008, SAF-REQ-029 | Safety-governed | Draft; policy approval pending where applicable |
| BR-017 | Risk assessment | Do not calculate risk using an independent unapproved model. | SAF-REQ-008, SAF-REQ-025 | System control | Draft; policy approval pending where applicable |
| BR-018 | Review and approval | Block submission with incomplete mandatory information. | SAF-REQ-010, SAF-REQ-023 | Safety-governed | Draft; policy approval pending where applicable |
| BR-019 | Review and approval | Restrict review decisions to authorized people. | SAF-REQ-011, SAF-REQ-025 | Safety-governed | Draft; policy approval pending where applicable |
| BR-020 | Review and approval | Communicate rejected plans and requested changes. | SAF-REQ-011 | Product | Draft; policy approval pending where applicable |
| BR-021 | Review and approval | Bind decisions to the applicable plan revision. | SAF-REQ-011, SAF-REQ-014, SAF-REQ-028 | System control | Draft; policy approval pending where applicable |
| BR-022 | Review and approval | Approval does not certify physical controls as implemented. | SAF-REQ-009, SAF-REQ-025 | Safety-governed | Draft; policy approval pending where applicable |
| BR-023 | Review and approval | Show outstanding obligations affecting readiness. | SAF-REQ-009, SAF-REQ-012 | Product | Draft; policy approval pending where applicable |
| BR-024 | SRB | Display the applicable SRB obligation. | SAF-REQ-009, SAF-REQ-029 | Product | Draft; policy approval pending where applicable |
| BR-025 | SRB | Attribute SRB decisions to authorized participants. | SAF-REQ-011, SAF-REQ-025, SAF-REQ-029 | Safety-governed | Draft; policy approval pending where applicable |
| BR-026 | SRB | Unresolved SRB decisions affect readiness according to approved transition rules. | SAF-REQ-012, SAF-REQ-029, SAF-REQ-030 | Safety-governed | Draft; policy approval pending where applicable |
| BR-027 | SRB | Distinguish SRB reassessment from ordinary plan revision. | SAF-REQ-013, SAF-REQ-029 | Safety-governed | Draft; policy approval pending where applicable |
| BR-028 | Permit to Work | Identify and link applicable permit requirements. | SAF-REQ-009, SAF-REQ-030 | Safety-governed | Draft; policy approval pending where applicable |
| BR-029 | Permit to Work | Use approved criteria to determine permit types. | SAF-REQ-009, SAF-REQ-030 | Safety-governed | Draft; policy approval pending where applicable |
| BR-030 | Permit to Work | Display permit status and unresolved permit actions. | SAF-REQ-009, SAF-REQ-020 | Product | Draft; policy approval pending where applicable |
| BR-031 | Permit to Work | Apply approved transition-specific permit conditions. | SAF-REQ-012, SAF-REQ-030 | Safety-governed | Draft; policy approval pending where applicable |
| BR-032 | Permit to Work | Re-evaluate permit impact after scope changes. | SAF-REQ-013, SAF-REQ-030 | Safety-governed | Draft; policy approval pending where applicable |
| BR-033 | LOTO | Link applicable isolation requirements to task and equipment. | SAF-REQ-009, SAF-REQ-030 | Safety-governed | Draft; policy approval pending where applicable |
| BR-034 | LOTO | Use independent verified isolation information. | SAF-REQ-009, SAF-REQ-025 | Safety-governed | Draft; policy approval pending where applicable |
| BR-035 | LOTO | Distinguish pending, verified and unknown isolation states. | SAF-REQ-009, SAF-REQ-012 | System control | Draft; policy approval pending where applicable |
| BR-036 | LOTO | Preserve isolation responsibility during shift/participant transfer. | SAF-REQ-017, SAF-REQ-030 | Safety-governed | Draft; policy approval pending where applicable |
| BR-037 | LOTO | Do not silently release isolation on interruption or closure. | SAF-REQ-013, SAF-REQ-030 | Safety-governed | Draft; policy approval pending where applicable |
| BR-038 | Task readiness | Identify missing prerequisites relevant to requested task transition. | SAF-REQ-012, SAF-REQ-030 | Safety-governed | Draft; policy approval pending where applicable |
| BR-039 | Task readiness | Check current authoritative prerequisite information. | SAF-REQ-012, SAF-REQ-027 | System control | Draft; policy approval pending where applicable |
| BR-040 | Task readiness | Explain refused transitions and required actions. | SAF-REQ-012 | Product | Draft; policy approval pending where applicable |
| BR-041 | Task readiness | Distinguish notices from binding restrictions. | SAF-REQ-012, SAF-REQ-030 | Product | Draft; policy approval pending where applicable |
| BR-042 | Task readiness | Re-evaluate safety readiness when relevant facts change. | SAF-REQ-013, SAF-REQ-019 | System control | Draft; policy approval pending where applicable |
| BR-043 | Revision | Evaluate relevant changes for effect on plan validity. | SAF-REQ-013 | Safety-governed | Draft; policy approval pending where applicable |
| BR-044 | Revision | Show required reassessment actions to users. | SAF-REQ-013 | Product | Draft; policy approval pending where applicable |
| BR-045 | Revision | Retain superseded decisions and historical assessments. | SAF-REQ-014, SAF-REQ-028 | System control | Draft; policy approval pending where applicable |
| BR-046 | Revision | Apply an approved review process to material changes. | SAF-REQ-011, SAF-REQ-013 | Safety-governed | Draft; policy approval pending where applicable |
| BR-047 | Revision | Identify the currently applicable plan and decision. | SAF-REQ-014, SAF-REQ-027 | System control | Draft; policy approval pending where applicable |
| BR-048 | Handover | Allow incoming participants to access applicable safety information. | SAF-REQ-017, SAF-REQ-020 | Product | Draft; policy approval pending where applicable |
| BR-049 | Handover | Carry outstanding controls, permits and isolation responsibilities into handover. | SAF-REQ-017, SAF-REQ-030 | Safety-governed | Draft; policy approval pending where applicable |
| BR-050 | Handover | Record required acknowledgment according to adopted policy. | SAF-REQ-017, SAF-REQ-030 | Safety-governed | Draft; policy approval pending where applicable |
| BR-051 | Handover | Never erase obligations or historical decisions through handover. | SAF-REQ-014, SAF-REQ-017 | System control | Draft; policy approval pending where applicable |
| BR-052 | Exceptions | Never show unsuccessful submission or approval as complete. | SAF-REQ-015, SAF-REQ-027 | System control | Draft; policy approval pending where applicable |
| BR-053 | Exceptions | Detect conflicts before indicating successful changes. | SAF-REQ-015, SAF-REQ-027 | System control | Draft; policy approval pending where applicable |
| BR-054 | Exceptions | Do not represent unknown controls as verified. | SAF-REQ-009, SAF-REQ-012 | Safety-governed | Draft; policy approval pending where applicable |
| BR-055 | Exceptions | Provide understandable reasons for rejected operations. | SAF-REQ-010, SAF-REQ-015 | Product | Draft; policy approval pending where applicable |
| BR-056 | Exceptions | Preserve recoverable and auditable decision history. | SAF-REQ-014, SAF-REQ-015 | System control | Draft; policy approval pending where applicable |
| BR-057 | Exceptions | Handle unavailable external dependencies using approved safe failure and recovery rules. | SAF-REQ-015, SAF-REQ-025 | System control | Draft; policy approval pending where applicable |
| BR-058 | Participant acknowledgment | Individually identify engineers named on the applicable plan. | SAF-REQ-017 | Product | Draft; policy approval pending where applicable |
| BR-059 | Participant acknowledgment | Provide access to the plan before individual acknowledgment. | SAF-REQ-017 | Product | Draft; policy approval pending where applicable |
| BR-060 | Participant acknowledgment | Record acknowledgment identity, revision and timestamp. | SAF-REQ-017 | System control | Draft; policy approval pending where applicable |
| BR-061 | Participant acknowledgment | Prevent proxy acknowledgment without explicitly approved delegation. | SAF-REQ-017, SAF-REQ-025 | Safety-governed | Draft; policy approval pending where applicable |
| BR-062 | Participant acknowledgment | Newly named engineers review and acknowledge under applicable policy. | SAF-REQ-017, SAF-REQ-030 | Safety-governed | Draft; policy approval pending where applicable |
| BR-063 | Participant acknowledgment | Require renewed acknowledgment for material revisions when policy requires. | SAF-REQ-013, SAF-REQ-017, SAF-REQ-030 | Safety-governed | Draft; policy approval pending where applicable |
| BR-064 | Participant acknowledgment | Show outstanding acknowledgments to leads and participants. | SAF-REQ-017, SAF-REQ-020 | Product | Draft; policy approval pending where applicable |
| BR-065 | Participant acknowledgment | Keep acknowledgment separate from plan approval, toolbox talk and start-work authorization. | SAF-REQ-011, SAF-REQ-017, SAF-REQ-025, SAF-REQ-030 | Safety-governed | Draft; policy approval pending where applicable |

## Cross-cutting policy notes

1. **Approval, SRB sign-off, individual acknowledgment, toolbox talk, PTW, LOTO and start-work authorization are distinct outcomes.** Never infer one from another.
2. **BR-058–065** reflect the approved *product intention* to support individual acknowledgment, but the exact start/restart/continuation gates, late joiners, solo-task minimum and reacknowledgment remain pending safety-policy decisions.
3. **BR-024–037 and BR-038–042** must be reconciled against the existing source adoption matrix before authorizing workflow restrictions. A historical permit-expiry notice-only policy must not be silently converted to a hard stop.
4. **BR-012–017** require an approved scoring methodology, risk thresholds, owner and tests.
5. **BR-006–011** require the exact controlled hazard question content, applicability and conditional mapping.
6. **BR-043–051** require confirmed revision/handover rules and safeguards for live isolations.

## Acceptance mapping rule

Each rule needs a test/scenario ID, expected outcome, decision reference and review evidence before moving from Draft to Approved. Tests will be mapped in [Verification & Acceptance](SAF-001-Verification-Acceptance.md). Open decisions are listed in [Decision Register](02-decision-register.md).

## Gap conclusion

All proposed **BR-001 through BR-065** are accounted for as numbered entries. This closes the *inventory drafting* part of REV-001; **REV-001 remains open for independent safety review, detailed rule-to-test evidence and final owner approval**.
