---
title: DDA Current Truth and Artifact Retrieval Layer Design Authorization
asset_type: human_decision_record
status: authorized_for_bounded_candidate_design
version: v0.1
owner: Emmanuel Olana
created: 2026-07-15
goal_id: CTR-01
decision_owner: Emmanuel Olana
candidate_sha: pending_freeze
runtime_claim: none
canon_claim: none
external_write_claim: none
---

# DDA Current Truth and Artifact Retrieval Layer Design Authorization

## Human Instruction

On 2026-07-15, Emmanuel authorized a fresh user-owned task to design the minimum DDA Current Truth and Artifact Retrieval Layer above the existing `runs/YYYY-MM-DD/` evidence history.

## Authorized Outcome

Produce a bounded, verifier-ready candidate that:

1. keeps dated run artifacts as immutable historical evidence;
2. makes active goals, owners, decisions, holds, next actions, artifact lineage, reviewed SHAs, superseded artifacts, and compact recovery bundles easy to retrieve across runs;
3. separates current-truth indexing, artifact registration, recovery bundles, and canon-promotion gates;
4. reuses existing source-index, manifest, decision-record, verifier, lineage, and five-file recovery patterns;
5. defines recovery and update burden measures; and
6. tests the proposed fields and retrieval model against real EXP-02-R1 evidence before implementation.

## Authorized Work

- Read repository governance and the named July 14 and July 15 evidence.
- Add review-only design, fixture, completion, manifest, and verifier-intake artifacts under `runs/2026-07-15/`.
- Run deterministic local consistency and integrity checks.
- Preserve the existing dirty worktree and avoid unrelated edits.

## Held Work

No live current-truth files, frontend, automation, external write, push, runtime activation, skill/eval or permanent-agent promotion, infrastructure, canon, PR, `main` promotion, or repo replacement is authorized.

No candidate may be treated as accepted until it is frozen at an exact commit SHA, independently reviewed, and then decided by Emmanuel for the stated scope.
