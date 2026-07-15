---
title: DDA Current Truth and Artifact Retrieval Layer Candidate
asset_type: architecture_candidate
status: proposed_review_only
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: CTR-01
approval_status: not_approved
candidate_sha: pending_freeze
runtime_claim: none
canon_claim: none
---

# DDA Current Truth and Artifact Retrieval Layer Candidate

## 1. Decision

Use a small, human-maintained projection layer above immutable `runs/YYYY-MM-DD/` evidence. Do not create a database, service, frontend, automation, or new authority tier.

The smallest later implementation would add three projection surfaces outside `runs/`:

```text
current/
|-- current-truth-index.md
|-- artifact-registry.md
`-- recovery-bundles/
    `-- <bundle-id>.md
```

Canon promotion remains in existing exact-SHA verifier returns and human decision records under `runs/`. The projection layer may point to those decisions but cannot create or upgrade one.

## 2. First Principles

1. `runs/` remains immutable historical evidence.
2. `current/` is a replaceable projection for retrieval, never proof by itself.
3. Every projected value must point to one or more exact run artifacts and, when available, the exact reviewed commit SHA.
4. Supersession changes retrieval priority; it never deletes or rewrites lineage.
5. Unknown and conflict states stay explicit.
6. Recovery bundles answer a bounded question; they are not another archive.
7. Human and verifier gates retain their existing authority and vocabulary.

## 3. Separation of Concerns

| Surface | One job | May contain | Must not do |
|---|---|---|---|
| Current-truth index | Answer what is active now | Goal, owner, decision, holds, next action, evidence pointer | Store full history or create acceptance |
| Artifact registry | Answer what artifact is current and how it descends | Stable ID, path, type, SHAs, review scope, lineage, supersession | Decide goal state or hide old artifacts |
| Recovery bundle | Answer one recovery query with a compact frozen pointer set | Query, snapshot, up to five primary files, optional references, burden result | Become a standing source of truth or compress physical-file counts |
| Canon-promotion gates | Decide whether reviewed material can advance | Existing verifier return plus explicit human promotion decision at exact SHA | Be inferred from `current/`, commit, push, recency, or candidate status |

## 4. Current-Truth Index Record

One row represents one active or recently decision-relevant goal. Closed goals leave the active view after their closure evidence and successor relationship are registered.

### Required fields

| Field | Meaning |
|---|---|
| `goal_id` | Stable goal-cycle identifier |
| `goal` | Observable outcome, not packet activity |
| `state` | `proposed`, `authorized`, `active`, `candidate_ready`, `verifier_review`, `human_decision`, `accepted`, `held`, `rework`, `rejected`, or `closed` |
| `goal_owner` | Person accountable for the outcome |
| `decision_owner` | Human authorized to accept, hold, rework, or reject |
| `current_decision` | Latest decision plus its exact scope |
| `holds` | Explicit unresolved blockers or prohibited progression; `none` only when evidenced |
| `next_action` | One concrete next action |
| `next_owner` | One owner for that action |
| `evidence_ref` | Highest-authority run artifact supporting the row |
| `reviewed_sha` | Exact reviewed candidate SHA, or `not_yet_frozen` / `not_applicable` |
| `bundle_id` | Default compact recovery bundle |
| `as_of` | Timestamp or date of the supporting decision event |
| `freshness` | `current`, `stale`, `held_conflict`, or `unknown` |

### Rules

- `state` and `current_decision` are separate. An artifact may be accepted for decision-readiness while runtime, canon, or promotion remains held.
- A later date does not automatically outrank a higher-authority decision.
- `stale` means newer material evidence exists or an explicit review-by condition expired. Age alone is not enough.
- `held_conflict` requires the conflicting references and a named resolution owner.
- Every active row has exactly one next action and next owner. Additional work stays in the goal-linked task ledger.

## 5. Artifact Registry Record

One row represents one physical repository artifact. Logical packets must list their physical files individually.

### Required fields

| Field | Meaning |
|---|---|
| `artifact_id` | Stable identifier independent of filename |
| `path` | Physical repo path |
| `artifact_type` | Existing type such as decision record, candidate, manifest, verifier return, scoreboard, or source index |
| `goal_id` | Owning goal cycle or `governance` |
| `source_run` | Dated run that first recorded the artifact |
| `evidence_sha` | Commit containing this exact artifact state, or `uncommitted_candidate` |
| `review_status` | `unreviewed`, `accepted`, `held`, `rework`, or `rejected` |
| `review_scope` | Exact scope of that status; never implied globally |
| `reviewed_sha` | Candidate SHA evaluated by the verifier/human decision, or `not_reviewed` |
| `lineage_parent` | Immediate predecessor artifact ID, or `none` |
| `supersedes` | Artifact ID displaced for retrieval, or `none` |
| `superseded_by` | New artifact ID, or `none` |
| `current_role` | `primary`, `supporting`, `historical`, or `held_conflict` |

### Lineage rules

- `lineage_parent` records derivation. `supersedes` records retrieval priority. They are not interchangeable.
- A rework result remains attached to its original candidate even if a later R1 artifact is accepted.
- `superseded_by` never changes the old artifact's review status.
- Rename or copy events require a new artifact ID only when the physical artifact or review identity changes; path-only movement preserves the ID and records the move in a dated run artifact.

## 6. Recovery Bundle

A bundle is assembled for a named query such as `recover current state of CTR-01` or `explain EXP-02-R1 lineage`. It contains:

1. `bundle_id`, query, goal ID, assembled date, and assembler;
2. a copied current-truth snapshot with evidence references;
3. up to five individually named primary physical files in open order;
4. optional secondary references that are not required for the bounded answer;
5. known conflicts, unknowns, and non-claims; and
6. measured recovery time and physical-file opens.

The five-file limit is a target inherited from the repo's fresh-recovery and EXP-02-R1 tests. If the answer needs more than five primary files, the bundle must report a burden failure rather than relabel multiple files as one packet.

## 7. Retrieval Queries

The minimum layer must answer these without scanning every dated folder:

| Query | Primary surface | Required answer |
|---|---|---|
| What goals are active? | Current-truth index | Goal, state, owner, decision, hold, next action |
| Who owns the next action? | Current-truth index | One next owner and evidence date |
| Why is this artifact current? | Artifact registry | Review scope, SHAs, lineage, supersession |
| What did this artifact replace? | Artifact registry | Predecessor and superseded artifact without status rewrite |
| What do I open to recover this goal? | Recovery bundle | Ordered maximum-five physical files and burden result |
| Can this become canon or runtime-ready? | Existing promotion gates | Exact verifier and human decision; default answer is held absent explicit authority |

## 8. Manual Update Protocol

Until the model is independently accepted and later authorized for implementation, no live projection files exist. If implementation is authorized, every material update follows this manual sequence:

1. Record the event in a new or active dated-run artifact; never rewrite earlier evidence.
2. Resolve authority and scope using `docs/source-authority-ladder.md`.
3. Update the current-truth row only when goal state, decision, hold, or next action changed.
4. Update registry rows only when a physical artifact, SHA, review scope, lineage, or retrieval priority changed.
5. Create or refresh a recovery bundle only for an actual handoff/recovery query.
6. Run deterministic checks for missing required fields, broken paths, impossible SHA/status combinations, cycles in supersession, more than one next owner, and bundles over five primary files.
7. Record update burden in the dated completion or verifier return.

## 9. Burden Measures

### Recovery burden

| Measure | Definition | Initial review threshold |
|---|---|---:|
| `recovery_elapsed_seconds` | Start at opening the bundle; stop when goal, owner, decision, holds, next action, lineage, and reviewed SHA are stated | `<= 600` |
| `primary_files_opened` | Individually opened physical files required for the answer | `<= 5` |
| `extra_searches` | Searches outside the bundle needed to answer | `0` |
| `unresolved_conflicts` | Material conflicts left without references and resolution owner | `0` |
| `unknown_required_fields` | Required fields still unknown after recovery | `0`, except explicitly inapplicable SHAs |
| `recovery_errors` | Incorrect state, scope, lineage, or promotion claims | `0` |

### Update burden

| Measure | Definition | Initial review threshold |
|---|---|---:|
| `update_elapsed_seconds` | Time from confirmed event evidence to completed projection checks | Observe on first three real updates; no improvement claim yet |
| `projection_files_touched` | Current index, registry, and any requested bundle | `<= 3` |
| `rows_changed` | Rows added or materially changed | Report, do not optimize yet |
| `manual_copy_fields` | Fields retyped instead of referenced | Report; prefer pointers over duplicated prose |
| `clarifications` | Human clarifications required only to maintain the layer | `0` target |
| `correction_cycles` | Corrections after deterministic checks | `0` target |
| `history_files_modified` | Previously recorded run artifacts edited by the projection update | `0` |

The next three real updates establish the burden baseline. No automation or improvement claim is justified before those observations exist.

## 10. Validation Sequence Before Build

1. Freeze this candidate and fixture at an exact commit SHA on a scoped branch.
2. An independent verifier checks field sufficiency, authority separation, lineage accuracy, five-file recovery, and burden calculations against the committed EXP-02-R1 data.
3. Emmanuel returns `accept`, `revise`, `hold`, or `reject` for implementation design only.
4. If accepted, manually implement only the three `current/` projection surfaces.
5. Run three real goal/update observations and independently review their accuracy and burden.
6. Only then may a separate human decision consider frontend or automation work.

## 11. Rejected Complexity

Not included: database schema, API, UI, search service, vector store, event bus, background sync, agent memory, cross-repo ingestion, permanent role assignment, or automatic canon promotion. None is required to test whether the fields and retrieval model are correct.

## 12. Proof Boundary

This is a review-only architecture candidate. It does not create a live current-truth layer, modify historical evidence, validate retrieval in runtime, authorize automation or frontend work, establish canon, approve infrastructure, promote a skill/eval/agent, open a PR, promote `main`, write externally, replace a repo, or prove operational improvement.
