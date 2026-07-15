---
title: DDA Current Truth and Artifact Retrieval Candidate Manifest
asset_type: candidate_manifest
status: ready_for_candidate_commit
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: CTR-01
candidate_sha: assigned_by_commit_containing_this_manifest
approval_status: not_approved
---

# DDA Current Truth and Artifact Retrieval Candidate Manifest

## Freeze Rule

The future scoped commit containing this manifest is the CTR-01 `candidate_sha`. The verifier must read the named files from that exact commit, confirm each listed SHA-256 value, and avoid the moving worktree. This manifest does not list its own hash because a file cannot contain its final self-hash.

## Candidate Files and Pre-Commit Hashes

| File | SHA-256 |
|---|---|
| `human-decision-record-current-truth-retrieval-layer-v0.1.md` | `FCC1AE4EF430CB7AAE37EA5238B9633861A6CB475591607CB0D7A0627C3FB087` |
| `current-truth-retrieval-source-index-v0.1.md` | `9537F78779B31652105E9806EA27898903E63BF1A50D2CD7AAE5188C8324C666` |
| `current-truth-retrieval-layer-candidate-v0.1.md` | `BD8C6F0B81361D74F279B6D559A2258CE0246DC28AC1DDA240CA05C5CDDDFCE8` |
| `current-truth-retrieval-layer-real-data-fixture-v0.1.md` | `DE73297FE9CF4A39A79430D55D90D03B3290039BDC03043BFB18455E4A85F330` |
| `current-truth-retrieval-layer-verifier-intake-v0.1.md` | `281DD732CA72EC1BA1BC7186391836F2DC099933C122A15E905A2834BAB03E1B` |
| `codex-to-dda-current-truth-retrieval-completion-v0.1.md` | `0304003BA8EAB2D373837C5A47ABE5F130458543AA6D622F4CE387E8AEBD86E2` |

All paths are relative to `runs/2026-07-15/`.

## Excluded Worktree State

All pre-existing changes to `AGENTS.md` and `runs/2026-07-14/` are excluded. No existing July 15 or earlier artifact is part of the change set.

## Proof Boundary

The manifest prepares a candidate freeze only. Commit, if later authorized, is transport and review evidence—not acceptance, canon, validation, runtime readiness, automation, frontend approval, infrastructure approval, skill/eval or agent promotion, PR or `main` approval, push, external posting, or repo replacement.
