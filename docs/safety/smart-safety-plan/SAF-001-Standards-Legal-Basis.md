# SAF-001 — Standards & Legal Basis Register (v0)

| Field | Value |
|---|---|
| Product / function | FabPilot / Safety |
| Feature | SAF-001 — Smart Safety Plan |
| Version / status | v0 — Draft, applicability not approved |
| Proposed accountable reviewers | Site EHS / Legal or Compliance / Product Owner |
| Related documents | [Executive PRD](SAF-001-Executive-PRD.md) · [Technical PRD](SAF-001-Technical-PRD.md) · [User Workflows](SAF-001-User-Workflows.md) |
| Assessment date | 2026-10-14 |

## 1. Purpose

Identify the potential sources of legal duties, technical safety guidelines and internal obligations relevant to **task-specific Safety Plan software**. This is an *applicability review register*, not a declaration of regulatory compliance.

**Boundaries:** A Safety Plan supports safe planning, traceable review and appropriate task authorization. It cannot substitute for legally required employer risk assessment, site procedures, physically verified energy isolation, competent supervision or work-equipment controls.

## 2. Source hierarchy

1. **Applicable law and enforceable regulations** in the jurisdiction and work situation.
2. **Binding contractual, customer and company requirements** when confirmed by an authorized owner.
3. **Technical standards / industry guidelines** only to the extent applicable or formally adopted by a binding obligation or approved project decision.
4. **Product design recommendations** until accepted into the product baseline.

If sources appear inconsistent, identify the specific clause and get competent legal/safety review. Do not infer that a guideline is automatically binding legislation.

## 3. Candidate external sources for applicability review

| ID | Source | Category | Potential relevance | Current disposition |
|---|---|---|---|---|
| STD-001 | Ireland — Safety, Health and Welfare at Work Act 2005 | Law | Employer duties, hazard identification and workplace risk assessments | Candidate; site/jurisdiction applicability to confirm |
| STD-002 | Ireland — Safety, Health and Welfare at Work (General Application) Regulations 2007, as amended | Regulations | Work equipment, electricity, PPE, work at height, pressure systems and other task hazards where relevant | Candidate; sections applicable per activity to confirm |
| STD-003 | SEMI S2-0724E, Environmental, Health, and Safety Guideline for Semiconductor Manufacturing Equipment | Industry guideline | Semiconductor equipment EHS considerations and equipment context | Candidate; applicability/adoption to confirm |
| STD-004 | SEMI S10-0526, Safety Guideline for Risk Assessment and Risk Evaluation Processes | Industry guideline | Potential risk assessment method for semiconductor manufacturing equipment | Candidate; methodology and adoption to confirm |
| STD-005 | Site / customer EHS procedures, LOTO, permit-to-work, emergency response and training instructions | Internal / customer | Binding site rules if adopted for the work | **Source documents not yet supplied** |
| STD-006 | Equipment manufacturer instructions and machine-specific hazard/control documentation | Equipment source | Work-specific hazards and required controls | **Source documents not yet supplied** |

**Source verification links (information only; not incorporated by blanket reference):**
- STD-001: https://www.irishstatutebook.ie/eli/2005/act/10/enacted/en/html
- STD-002: https://www.irishstatutebook.ie/eli/2007/si/299/
- STD-002 HSA guidance: https://www.hsa.ie/topics/managing_health_and_safety/general_application_regulations_2007/
- STD-003 SEMI: https://store-us.semi.org/products/s00200-semi-s2-environmental-health-and-safety-guideline-for-semiconductor-manufacturing-equipment
- STD-004 SEMI: https://store-us.semi.org/products/s01000-semi-s10-safety-guideline-for-risk-assessment-and-risk-evaluation-process

External links verify the *identity and scope* of potential sources; they do not establish legal applicability, an accepted risk matrix or requirements for every activity.

## 4. Requirement-to-obligation mapping (proposed)

| SAF requirement | Obligation to confirm | Evidence needed | Status |
|---|---|---|---|
| SAF-REQ-004–007, 021 | Controlled pre-task questions reflect applicable hazards and company/site assessments | Authorized 12-question catalogue and source mapping | Open |
| SAF-REQ-008, 028 | Risk estimation, classification and acceptance reflect adopted methodology | Approved risk method, severity/likelihood scales, thresholds | Open |
| SAF-REQ-009, 025, 030 | PTW, isolation, PPE, SRB and competence gates reflect applicable rules | Site procedures, approval matrix, per-task applicability | Open |
| SAF-REQ-010–012 | Submission, approval and work-authorisation checks reflect approved responsibilities | Signed authority and transition rules | Open |
| SAF-REQ-013–015, 027–029 | Revisions and historical decisions maintain safety relevance | Revision/expiry triggers, records and audit requirements | Open |
| SAF-REQ-016, 031 | Accessibility and hazard-symbol presentation are appropriate | Design review and icon source/provenance | Open |
| SAF-REQ-017, 020 | Shift changes and task execution keep obligations visible | Handover process and Task Workspace acceptance tests | Open |

## 5. Applicability decision template

For each source, the Safety/Compliance Owner records:
- **Jurisdiction and operational scope:** site, employer, asset type, task category, contractor/customer relationships.
- **Precise provision:** named clause/section and current revision, not just standard title.
- **Status:** Applicable / Not applicable / Contractually adopted / Informative / Under review.
- **Reason:** documented applicability rationale and precedence decision.
- **Product effect:** mapped SAF-REQ IDs and resulting business rule, if any.
- **Approval and evidence:** reviewer name/role, date, approval record and change trigger.

No catalog rule, risk score, PTW or isolation state should be hard-coded solely from this draft register.

## 6. Workflow and change control

1. Identify the task scenario and equipment hazards; capture the relevant work jurisdiction.
2. Check each candidate source and its applicability with a qualified site authority.
3. Record concrete requirements and decisions in the register and [Decision Register](02-decision-register.md).
4. Trace the approved requirement to the [Technical PRD](SAF-001-Technical-PRD.md), hazard catalogue and acceptance cases.
5. Review updates when legislation, standards, site processes, equipment or product functions change.

## 7. Open gates

- [ ] Confirm launch jurisdiction(s), employers, customer/site responsibilities and equipment categories.
- [ ] Verify precise statutory duties and adopted industry standard revisions against authoritative source copies.
- [ ] Obtain applicable site PTW, LOTO, SRB, training and emergency requirements.
- [ ] Approve hazard screening, risk methodology and risk acceptance thresholds.
- [ ] Map applicable obligations to individual SAF-REQ IDs and test evidence.
- [ ] Obtain sign-off from qualified Safety/Compliance Owner.

**Release rule:** This draft does not confer legal compliance or authority to operate. Approved obligations and documented safe systems of work remain prerequisites for operational release.
