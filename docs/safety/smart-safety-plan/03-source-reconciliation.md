# SAF-001 — Historical Source Reconciliation

**Status:** Working evidence, not an adopted safety standard or current greenfield architecture.  
**Current historical main checked:** `sagrado26/fabpilot-fsm@9518807a31e9e751f7dcbb9bc71d226ad461a633`.

**Authority level:** This is a candidate product contract, not an approval of historical FabPilot engineering decisions. The greenfield architecture remains independently selectable. Historical implementation is examined for coverage and failure modes, **not copied**.

### Sources examined

| Source | Source authority for this draft | Verified evidence |
|---|---|---|
| FabPilot `main` at `9518807a31e9e751f7dcbb9bc71d226ad461a633` | Historical application snapshot | Verified GitHub comparison identical to current main during review |
| PR #176 `Documentation/smart-forms/CONSOLIDATION-2026-10-13.md` | Historical reconciliation proposal | Four-stage owner intent, branch conflicts, unqualified integration |
| PR #179 `Documentation/audits/SAFETY-CANONICAL-PAGE-INVENTORY-2026-10-13.md` | Historical audit/candidate | Reusable form framework; 12 questions not controlled; backend safety boundaries |
| PR #181 `Documentation/smart-forms/SAFETY-PLAN-INTEGRATION.md` | Unmerged technical candidate | Conditional answer retention, explicit clearing, incomplete drafts, server authorization |
| PR #177 `App files/src/active-ui/SmartSafetyPlanBuilder/README.md` | Unmerged design candidate | Governed builder, preview and publish boundaries |
| Copied historical reconciliation and owner-rulings documents in `references/` | Historical decision evidence | SRB, PTW and acknowledgment details require adoption decisions |

**Source limitation:** The original 425-line external ISP specification was not available in full readable form in this reconciliation. This document must not claim exact source-to-requirement completeness.

### Confirmed product intent versus proposals

| Aspect | Preserved owner intent | Undecided / requiring approval |
|---|---|---|
| UX | One task-linked four-stage plan: pre-task details; hazard screening; risk assessment; review/sign-off | Exact stage labels and mandatory input conditions |
| Screening | 12 intended pre-task questions with compact Yes→hazard selection | Approved question wording, number of currently active records, mappings and catalogue ownership |
| Hazard guidance | Show hazards, undesired events/outcomes, baseline controls progressively | Authority/provenance of ISO/GHS icons and any mapping not yet approved |
| Risk | Show initial/residual risk and task-specific controls without a second risk model | Methodology, escalation thresholds, independence and acceptance |
| Forms | Reusable builder, conditional questions, preview and controlled publication | Builder permissions, published schema contracts and migration policy |
| Workflow | Connect Safety Plan with Tasks, readiness, PTW, LOTO, PPE, SRB, competency and audit | Exact terminal outcomes, permit lifecycle and approval/acknowledgment policy |
| Rendering | Light enterprise UI, compact and responsive, visual awareness within Task Workspace | Definitive screen-level design and accessibility evidence |



## Requirement changes incorporated into the PRD

The following draft requirement IDs were preserved and consolidated into the single requirement table in [Technical PRD §3](SAF-001-Technical-PRD.md#3-detailed-requirement-register): **SAF-REQ-021 through SAF-REQ-032**. They remain proposals until product and safety approval.

## Specific safety-policy conflicts and boundaries

The copied historical owner rulings contain nuanced behaviour, including one-person-task acknowledgment, SRB reassessment, permit expiry notices, permit duration, and interaction of live permits with plan revision. **Do not replace these with an invented generic “always hard stop” rule.** Equally, historical rulings are **not automatically adopted** for FabOps-Green. For each case, record: source rule → safety consequence → proposed greenfield rule → authority signoff → acceptance test.

## Evidence and limitations

The original 425-line external ISP specification has **not** been reconciled line by line. Open PR implementations are unmerged candidates, not production authority. The owner must decide how to adopt or reject each historical PTW/SRB/acknowledgment rule. Never seed missing hazard definitions or invent risk ratings to fill documentation gaps.

Read [historical references](references/README.md) and the [decision register](02-decision-register.md).
