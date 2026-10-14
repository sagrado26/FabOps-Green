> Historical source copy from `sagrado26/fabpilot-fsm/Ref files/handoff-notes/2026-10-04-srb-ptw/owner-rulings.md` (retrieved 2026-10-14). Preserved as reference only. This is NOT an approved greenfield requirement, architecture decision or evidence that the behavior is implemented in FabOps-Green. Reconcile each rule before adoption.

---

# Owner rulings on SRB and acknowledgement questions (4 October 2026)

These answer the open questions in srb-ack-plan.md. Q2, Q3, Q8, Q9 and Q10 were not answered and use the plan's recommended defaults.

- Q1: The Action Lead acknowledgement stays mandatory. Named people add acknowledgements; they do not replace it.
- Q4: The submitter is auto-acknowledged at submission. The submitter counts only if they are the lead or an active team member.
- Q5: A one-person task CAN start. The Action Lead acknowledgement is what is required. Tasks already in progress are not re-gated.
  Interpretation to confirm: the "at least one other named member" half of the minimum applies only when the plan names other
  members. A plan with no other named member needs only the Action Lead acknowledgement.
- Q6: One person cannot record two SRB parties (add a guard; today the unique key allows it).
- Q7: SRB-006 (an SRB approval amending the plan) is not adopted. The SRB process is a re-assessment of the submitted Safety Plan's
  Risk Assessment. Keep the revise-to-low risk assessment mechanism; do not create a plan revision on SRB approval.
- Already ruled earlier: any person named on the SRB may acknowledge it; the SRB follows the ISP specification; the toolbox talk is
  record-only; the risk assessment gate on plan submission stays.

# Owner rulings on PTW questions (4 October 2026)

Answers to the seven questions in ptw-workflow-survey.md section 6.

- PTW-005, permit expires while work runs: notify users only. Send an alert and show a derived "required permit lapsed" flag.
  No hard stop, no StopTheJob, no hold state.
- PTW-007 / EXE-005: do NOT block lock removal or isolation release while a permit is live. Widen ClosePermit so the task lead,
  the action lead and other persons listed on the plan may close a permit.
- Revising an approved plan does NOT close its live permits. The risk assessment in the plan is a live document and permits must not
  depend on plan changes. Permits are affected only by the terminal outcomes the spec names (PTW-004 plan closed, PTW-006 plan
  rejected or cancelled before use). Assumption to confirm: an SRB return that rejects an approved plan is such a terminal outcome.
- Duration: the approved duration is required (minimum 60 minutes), valid_until is derived from it, and an optional site maximum
  stays unset until the site supplies one.
- A plan's permit clarification answered "Required" names a permit type from the six, creates a requirement and gates StartWork.
- IssuePermit stays L2-only and is not gated on the acknowledgement minimum. There is no separate plan "cancel" command
  (AbortTask already closes plans and permits).
- Vocabulary (question 3) was not answered: keep `closed` plus close_reason and the existing `suspended` state; no migration.

- Confirmed by the owner (4 October 2026): an SRB return that rejects an approved plan is a terminal outcome (PTW-006), so it voids that plan's live permits.
