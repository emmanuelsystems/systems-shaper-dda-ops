---
title: DDA Current Truth and Artifact Retrieval Layer Source Index
asset_type: run_source_index
status: candidate_packet_ready_for_freeze
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: CTR-01
parent_sha: 66f52f5f31dcb370645a52795ea9f6ec220b866c
candidate_sha: pending_freeze
approval_status: not_approved
runtime_claim: none
canon_claim: none
---

# DDA Current Truth and Artifact Retrieval Layer Source Index

## Purpose

Route one review-only design cycle for the minimum layer that retrieves current operational truth from immutable dated-run evidence. This scoped source index is additive. It does not modify or supersede the existing EXP-02 source index or any earlier run artifact.

## Goal

`CTR-01`: Define the smallest independently reviewable field and retrieval model for cross-run current truth and artifact recovery, using accepted EXP-02-R1 evidence as the real-data test, before any live layer, frontend, or automation is built.

## Governing Sources

| Source | Use | Authority or limitation |
|---|---|---|
| `AGENTS.md` | Repo rules, read order, proof boundaries, and dated-run write target | Current workspace governance; existing dirty change preserved |
| `README.md` | Repo role and fresh recovery path | Current governance |
| `docs/source-of-truth.md` | Durable-truth and human-gate rules | Current governance |
| `docs/source-authority-ladder.md` | Claim authority, exact-SHA rules, and conflict handling | Current governance |
| `runs/2026-07-14/mta-analysis-v0.1.md` | Evidence-backend, goal-centered orchestration, compact-view direction, and frontend hold | July 14 analysis candidate; not approval by itself |
| `runs/2026-07-14/codex-multi-conversation-structure-v0.1.md` | Required current state, lineage, verifier, and human-role model | Proposed review-only architecture evidence |
| `runs/2026-07-15/source-index.md` | Current EXP-02/R1 routing and accepted-scope statement | Current committed dated routing evidence |
| `runs/2026-07-15/exp-02-r1-verifier-return-v0.1.md` | Independent accepted decision-readiness result at exact SHA | Accepted for stated review scope only |
| `runs/2026-07-15/exp-02-r1-human-decision-record-v0.1.md` | Human acceptance and remaining holds | Highest current decision authority for R1 scope |
| `runs/2026-07-15/exp-02-r1-final-scoreboard-v0.1.md` | Recovery and coordination burden observations | Calibration evidence; operational improvement not proven |
| `runs/2026-07-15/dda-optimization-target-v0.1.md` | Working goal-cycle unit, outcome metrics, guardrails, and minimum trace | Working experiment target; not canon or runtime policy |
| `human-decision-record-current-truth-retrieval-layer-v0.1.md` | Current design authorization and held scope | Current human instruction captured for this packet |

## Candidate Packet

| Artifact | Role |
|---|---|
| `current-truth-retrieval-layer-candidate-v0.1.md` | Proposed topology, fields, retrieval rules, update protocol, and gates |
| `current-truth-retrieval-layer-real-data-fixture-v0.1.md` | Filled EXP-02-R1 and CTR-01 records plus a compact recovery bundle |
| `current-truth-retrieval-candidate-manifest-v0.1.md` | Exact review-set file hashes before commit |
| `current-truth-retrieval-layer-verifier-intake-v0.1.md` | Independent review contract, thresholds, and return shape |
| `codex-to-dda-current-truth-retrieval-completion-v0.1.md` | Scope, checks, limitations, and next gate |

## Conflict Rule

The current-truth layer is a derived routing projection, not a new authority tier. When sources conflict, the higher source-authority record wins only within its stated scope. Equal-authority or scope-ambiguous conflicts remain explicit `held_conflict`; no value is averaged or silently overwritten.

## Historical-Evidence Rule

Existing `runs/` files are inputs, not mutable current-state records. This packet adds new evidence for the July 15 work cycle and proposes future projections outside `runs/`. It does not rewrite any prior artifact, verifier result, human decision, or superseded candidate.

## Proof Boundary

The packet is local, uncommitted candidate evidence until frozen. No implementation, acceptance, canon, validation, runtime readiness, automation, frontend, external write, push, PR, `main`, infrastructure, skill/eval or permanent-agent promotion, or repo replacement is claimed.
