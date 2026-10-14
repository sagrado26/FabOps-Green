# SAF-001 — Open Decision Register

**Status:** Unresolved; decisions below are *not* approved. This register is the only home for SAF-DEC items.

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

The eight decisions in §8 remain open. Additionally resolve:
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

**Baseline status: BLOCKED until review and open decisions are resolved.**

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
