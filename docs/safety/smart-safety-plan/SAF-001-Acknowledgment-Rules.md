# SAF-001 — Safety Plan Acknowledgment Rules (v0)

**Status:** Draft, proposed process rules pending Safety Authority approval. This is part of the SAF-001 baseline and not a separate feature approval.

## Purpose and distinctions

Named engineers who participate in task execution need access to, understanding of and attributable acknowledgment of the applicable Safety Plan. Individual acknowledgment does **not** replace (1) authorized plan approval, (2) toolbox-talk attendance, or (3) independent start-work authorization/physical-control verification.

## Business rules

| Rule | Description | SAF-REQ |
|---|---|---|
| BR-058 | Identify every named engineer individually | 017 |
| BR-059 | Provide access to current applicable plan before acknowledgment | 017 |
| BR-060 | Record actor, revision and timestamp for each acknowledgment | 017 |
| BR-061 | Do not allow one engineer to sign for another absent an explicitly approved delegation | 017 |
| BR-062 | Newly joining engineers must review and acknowledge under applicable policy | 017, 030 |
| BR-063 | Material revision may require renewed acknowledgment under policy | 017, 030 |
| BR-064 | Show missing acknowledgments to Action Lead and participants | 017 |
| BR-065 | Distinguish acknowledgment from approval, toolbox talk and work authorization | 017, 030 |

## Candidate participation policy — not yet approved

- Action Lead acknowledgment is mandatory under the historical model.
- A single-engineer task can satisfy the acknowledgment minimum with the Action Lead alone.
- Other named engineers add personal acknowledgment obligations; they do not replace the lead's acknowledgment.
- In-progress work should not be automatically re-gated solely due to acknowledgment changes; precise triggers require policy.
- The exact rule for initial Start Work, restart, joining after work began, removals and material revision is **TBD**.
- Existing FabPilot historical rulings are review inputs only, not adopted greenfield policy.

## Required acceptance scenarios

Solo engineer, two engineers, named engineer absent, late joiner, changing lead, revision after acknowledgment, shift transfer, attempted proxy acknowledgment, conflict/stale revision, already-running work and failed recording.

See [Technical PRD](SAF-001-Technical-PRD.md) and [acknowledgment swimlane](SAF-001-User-Workflows.md).