# SAF-001 — Authoritative Decision Register

**Version:** v0 · Updated 2026-10-14 · **Product direction:** 8/8 confirmed by Product Owner in conversation · **Safety approval:** Pending.

Only this file records SAF-DEC decision dispositions. Product decisions establish intended functionality; they do not approve risk controls, legal applicability, physical isolation, or operational release.

## Confirmed product decisions

| ID | Confirmed direction | Status | Remaining governance boundary |
|---|---|---|---|
| SAF-DEC-001 | Controlled baseline of 12 pre-task questions; authorized safety admins may propose, review, approve and publish versioned changes. | Product decision confirmed | Exact question wording, mappings and approving safety authority remain open. |
| SAF-DEC-002 | Use existing FabPilot severity 1–3 × likelihood 1–4, highest individual risk roll-up and SRB trigger at index ≥6. | Product decision confirmed | Risk bands, acceptance/escalation and formal safety approval still require validation. |
| SAF-DEC-003 | Apply a centrally governed global baseline plus applicable legal, site, customer and equipment requirements approved by safety authorities. | Product decision confirmed | Determine source provisions and actual applicability before operational use. |
| SAF-DEC-004 | SRB, PTW and LOTO are separate governed lifecycles integrated with the Safety Plan and Task readiness. | Product decision confirmed | Transition rules for expiry, suspension, start, restart, continuation and closure remain open. |
| SAF-DEC-005 | Eligible personnel can prepare and submit; review and approval use an explicit authority matrix; Action Lead and named engineers acknowledge individually. | Product decision confirmed | Detailed approver eligibility, separation of duties and acknowledgment gating unresolved. |
| SAF-DEC-006 | Action Lead decides whether reassessment is needed, subject to mandatory escalation triggers; record the decision and rationale. | Product decision confirmed | Escalation triggers and safety impact of already-running work require safety approval. |
| SAF-DEC-007 | Standard audit history: actors, timestamps, plan versions, approvals/rejections and individual acknowledgments, with role-based access. | Product decision confirmed | Applicable retention, security and mandatory legal evidence requirements remain binding; enhanced signature/legal-hold features not initially scoped. |
| SAF-DEC-008 | Standard software release: functional testing and Product Owner acceptance; no blanket mandatory pilot or extra project-level safety release ceremony. | Product decision confirmed | Applicable law, site safety approval, verified operational safeguards and release authorization cannot be waived. |

## Remaining questions

The eight product direction decisions are confirmed above. Additionally resolve:
- **SAF-DEC-009:** exact field mandatory/conditional rules and defaults.
- **SAF-DEC-010:** draft/submit/reject/revise lifecycle and historical snapshot rules.
- **SAF-DEC-011:** what changed inputs invalidate approvals/readiness, including catalogue migrations.
- **SAF-DEC-012:** what counts as independent verification of linked physical safety controls.
- **SAF-DEC-013:** offline behaviour, fail-safe rules and retention of unsent drafts.
- **SAF-DEC-014:** treatment of hazards marked not applicable, unknown, or not covered by mappings.

### Approval checklist
- [ ] Product owner accepts scope and four-stage workflow
- [ ] Exact 12 screening questions and approved mapping source supplied
- [ ] Risk method and authority documented, including escalation thresholds
- [ ] Standards applicability reviewed; binding requirements distinguished from guidance
- [ ] Approval/competence matrix and lifecycle rules accepted
- [ ] Data, integrations, security, failure behaviour and historical records reviewed
- [ ] E2E and negative-path acceptance scenarios signed off

**Baseline status: Product direction confirmed; safety and implementation gates remain open.**

## Candidate decisions from legacy reconciliation

- **SAF-DEC-015:** Adopt the intended 12-question experience as exactly 12 mandatory governed questions, or allow a versioned configurable number with a validated baseline of 12?
- **SAF-DEC-016:** Which hidden-answer preservation/explicit-clear policy and migration rules are binding?
- **SAF-DEC-017:** Is a reusable governed form builder in the first release or an incremental release, with versioned publication before live use?
- **SAF-DEC-018:** Which historical owner rulings are formally adopted for SRB acknowledgment, PTW duration/expiry, and permit behaviour on revision/termination?
- **SAF-DEC-019:** What are the exact plan/task statuses and reauthorization boundaries for already-running versus newly-starting work?
- **SAF-DEC-020:** What is the approved asset/icon mapping and source of hazard presentation information?
- **SAF-DEC-021:** What is the canonical SRB/PTW/LOTO relationship to the plan, and where is each independent authority enforced?

## Resolution record (complete when decided)

For each decision, record: **Decision ID | Approved resolution | Approver | Date | Evidence link | Impacted SAF-REQ IDs | Tests | Status**. Do not treat a proposal or a previous repo ruling as accepted without explicit authorization.

