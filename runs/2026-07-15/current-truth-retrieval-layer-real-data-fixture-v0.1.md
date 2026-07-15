---
title: DDA Current Truth and Artifact Retrieval Real-Data Fixture
asset_type: review_fixture
status: proposed_review_only
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: CTR-01
source_goal_id: EXP-02-PM2E-2026-07-15
candidate_sha: pending_freeze
approval_status: not_approved
---

# DDA Current Truth and Artifact Retrieval Real-Data Fixture

## 1. Purpose

Test the proposed fields with actual committed EXP-02-R1 evidence and the current CTR-01 design authorization. This fixture is review data, not a live projection and not a rewrite of historical artifacts.

## 2. Current-Truth Rows

| goal_id | goal | state | goal_owner | decision_owner | current_decision | holds | next_action | next_owner | evidence_ref | reviewed_sha | bundle_id | as_of | freshness |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| `CTR-01` | Independently review the minimum current-truth and retrieval fields using real EXP-02-R1 data before implementation | `candidate_ready` | Emmanuel Olana | Emmanuel Olana | Design authorized only; candidate not accepted | Exact-SHA freeze, independent review, human implementation decision; all build, frontend, automation, external, runtime, promotion, and canon actions held | Freeze only the scoped candidate packet, then dispatch read-only verification | Root Orchestrator | `human-decision-record-current-truth-retrieval-layer-v0.1.md` | `not_yet_frozen` | `RB-CTR-01-V0.1` | `2026-07-15` | `current` |
| `EXP-02-PM2E-2026-07-15` | Establish a repeatable, review-only post-meeting-to-execution sequence that converts source-backed meeting direction into one measurable implementation goal, complete owner-tagged tasks, an unsent progress update, and one explicit human decision | `closed` | Emmanuel Olana | Emmanuel Olana | EXP-02-R1 accepted for bounded decision-readiness only | Runtime, canon, frontend, automation, infrastructure, promotion, repo replacement, and operational-improvement claims held | Use as calibration evidence; design the next real non-meta goal cycle with prospective instrumentation | Emmanuel Olana | `exp-02-r1-human-decision-record-v0.1.md` | `7437f21e0a5461ee559196f36f145cae41b4caa2` | `RB-EXP-02-R1-V0.1` | `2026-07-15` | `current` |

The EXP-02 row is shown because it remains decision-relevant calibration evidence. A live active-goal view may omit it after its successor link and retrieval bundle are registered.

## 3. Artifact Registry Rows

| artifact_id | path | artifact_type | goal_id | source_run | evidence_sha | review_status | review_scope | reviewed_sha | lineage_parent | supersedes | superseded_by | current_role |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| `ART-EXP02-C0` | `runs/2026-07-15/exp-02-post-meeting-execution-candidate-v0.1.md` | execution candidate | `EXP-02-PM2E-2026-07-15` | `2026-07-15` | `bc4b4cc401fd05b0311928a5a2fb87fa9f12eaf5` | `rework` | Original EXP-02 decision-readiness | `bc4b4cc401fd05b0311928a5a2fb87fa9f12eaf5` | `none` | `none` | `ART-EXP02-R1-C1` | `historical` |
| `ART-EXP02-R1-C1` | `runs/2026-07-15/exp-02-r1-post-meeting-execution-candidate-v0.1.md` | execution candidate | `EXP-02-PM2E-2026-07-15` | `2026-07-15` | `7437f21e0a5461ee559196f36f145cae41b4caa2` | `accepted` | R1 decision-readiness only | `7437f21e0a5461ee559196f36f145cae41b4caa2` | `ART-EXP02-C0` | `ART-EXP02-C0` | `none` | `primary` |
| `ART-EXP02-R1-V1` | `runs/2026-07-15/exp-02-r1-verifier-return-v0.1.md` | verifier return | `EXP-02-PM2E-2026-07-15` | `2026-07-15` | `005e45389818bffe1ba1a0b21ffa0c6f975b2848` | `accepted` | Independent R1 decision-readiness only | `7437f21e0a5461ee559196f36f145cae41b4caa2` | `ART-EXP02-R1-C1` | `none` | `none` | `primary` |
| `ART-EXP02-R1-D1` | `runs/2026-07-15/exp-02-r1-human-decision-record-v0.1.md` | human decision record | `EXP-02-PM2E-2026-07-15` | `2026-07-15` | `66f52f5f31dcb370645a52795ea9f6ec220b866c` | `accepted` | Bounded decision-readiness only | `7437f21e0a5461ee559196f36f145cae41b4caa2` | `ART-EXP02-R1-V1` | `none` | `none` | `primary` |
| `ART-DDA-TARGET-V0.1` | `runs/2026-07-15/dda-optimization-target-v0.1.md` | optimization target | `governance` | `2026-07-15` | `66f52f5f31dcb370645a52795ea9f6ec220b866c` | `unreviewed` | Human-directed working experiment target; no separate verifier result | `not_reviewed` | `ART-EXP02-R1-D1` | `none` | `none` | `supporting` |
| `ART-CTR01-C1` | `runs/2026-07-15/current-truth-retrieval-layer-candidate-v0.1.md` | architecture candidate | `CTR-01` | `2026-07-15` | `uncommitted_candidate` | `unreviewed` | Current-truth and retrieval design only | `not_reviewed` | `none` | `none` | `none` | `primary` |

### Fixture interpretation

- The original EXP-02 candidate remains `rework`; R1 does not rewrite it.
- R1 is both a lineage child and the retrieval successor of the original candidate.
- The R1 verifier and human decisions are separate physical artifacts with different authority and scope.
- The DDA target is a human-directed working definition, not independently accepted canon.
- CTR-01 has no reviewed SHA until a scoped candidate commit exists.

## 4. Recovery Bundle: `RB-EXP-02-R1-V0.1`

- Query: `Recover the current EXP-02/R1 goal outcome, owner, decision, holds, next action, lineage, and reviewed SHA.`
- Assembled: `2026-07-15`
- Assembler: Root Orchestrator
- Goal: `EXP-02-PM2E-2026-07-15`
- Expected answer: R1 is human-accepted for bounded decision-readiness only at reviewed SHA `7437f21e0a5461ee559196f36f145cae41b4caa2`; the original remains `rework`; all runtime, canon, promotion, and operational-improvement claims remain held; the next action is a separately authorized real non-meta goal cycle with prospective instrumentation.

### Primary open order

1. `runs/2026-07-15/source-index.md`
2. `runs/2026-07-15/exp-02-r1-human-decision-record-v0.1.md`
3. `runs/2026-07-15/exp-02-r1-verifier-return-v0.1.md`
4. `runs/2026-07-15/exp-02-r1-candidate-manifest-v0.1.md`
5. `runs/2026-07-15/dda-optimization-target-v0.1.md`

### Secondary references

- `runs/2026-07-15/exp-02-verifier-return-v0.1.md` for original defect detail.
- `runs/2026-07-15/exp-02-r1-final-scoreboard-v0.1.md` for measured R1 burden.

### Known limitations

- The bundle has not yet been independently timed from a frozen CTR-01 candidate SHA.
- The accepted R1 verifier measured `184.994 ms` across five physical files for its narrower recovery task. That result is calibration evidence, not this bundle's result.
- Numeric manual baseline and operational improvement remain unknown or unproven.

## 5. Recovery Bundle: `RB-CTR-01-V0.1`

- Query: `Recover the current CTR-01 design decision and next gate.`
- Expected answer: design-only authorization exists; the candidate is local and unreviewed; implementation and all promotion/runtime work remain held; the next gate is exact-SHA freeze and independent review.

### Primary open order

1. `runs/2026-07-15/current-truth-retrieval-source-index-v0.1.md`
2. `runs/2026-07-15/human-decision-record-current-truth-retrieval-layer-v0.1.md`
3. `runs/2026-07-15/current-truth-retrieval-layer-candidate-v0.1.md`
4. `runs/2026-07-15/current-truth-retrieval-layer-real-data-fixture-v0.1.md`
5. `runs/2026-07-15/current-truth-retrieval-layer-verifier-intake-v0.1.md`

## 6. Fixture Checks Required

An independent verifier must confirm:

1. every required field can be populated without inventing authority;
2. the original and R1 statuses remain distinct;
3. `lineage_parent` and `supersedes` are used correctly;
4. reviewed SHA and review scope are not conflated with artifact recency;
5. the five-file bundle yields the expected answer without extra search;
6. closed calibration evidence can be removed from the active view without losing retrieval; and
7. no projection field implies canon, runtime readiness, or operational improvement.

## 7. Proof Boundary

This fixture demonstrates proposed field usage only. It is not a live index, accepted schema, validated recovery result, frontend data model, automation input, canon registry, or runtime state.
