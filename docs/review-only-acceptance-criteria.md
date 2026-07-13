# Review-Only Operating-Layer Acceptance Criteria

Status: `candidate_review_only`

These criteria define what an independent verifier should check before accepting `systems-shaper-dda-ops` for review-only operating-layer use. Satisfying them does not make the repo accepted infrastructure, canon, or runtime-ready.

## Required Criteria

1. **Role clarity:** The repo is identified as the intended review surface for the manual DDA operating model, while `dda-agent-ops` remains the active pilot and evidence repo.
2. **Proof boundary:** No PR, `main`, replacement, runtime, canon, automation, memory, skill, eval, or Context Vault claim is implied.
3. **Source authority:** Navigation order and claim authority are separated, and conflicts are named rather than averaged.
4. **SHA traceability:** The return identifies the exact `parent_sha`, `reviewed_sha`, and frozen `candidate_sha`; the independent verifier names the exact candidate it reviewed.
5. **Recovery burden:** A fresh reviewer can recover the current state from five or fewer named artifacts with a target burden of Low.
6. **Decision ownership:** The implementation owner, independent verifier, and human promotion gate are explicit.
7. **Independent verification:** The implementation return does not verify itself. A separate reviewer returns accepted, held, rework, or rejected for the frozen candidate.
8. **Branch posture:** The bootstrap branch and absence of PR / `main` promotion are explicit; branch transport is not treated as acceptance.
9. **Transferability wording:** Commit `94e4775` is described as an accepted metadata clarification supporting a Narrow Pass for that handoff only; broader metadata policy and workflow acceptance remain held.

## Acceptance Result

The independent verifier may return `accepted for review-only operating-layer use` only when every required criterion is satisfied for the named `candidate_sha` with no unresolved contradiction. Otherwise the result must remain held, rework, or rejected with the missing criterion identified.

## Separate Gates

Review-only acceptance does not authorize a PR, `main`, migration, automation, memory, skill, eval, canon, Context Vault, or runtime movement. Each requires its own explicit scope, evidence, and human approval.
