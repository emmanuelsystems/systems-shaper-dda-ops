---
title: EXP-03 Human Authorization Record
asset_type: human_authorization_record
status: authorized_for_review_only_execution
version: v0.1
owner: Emmanuel Olana
created: 2026-07-15
goal_id: EXP-03-DDA-IMPLEMENTATION-DECISION-2026-07-15
decision_owner: Emmanuel Olana
external_write_claim: none
---

# EXP-03 Human Authorization Record

## Human Intent

Emmanuel authorized a fresh task to define and run EXP-03 as the first real, non-meta DDA goal cycle and prospective baseline observation 1 of 3. The root must select the highest-value real outcome supported by current repo evidence, freeze the goal and instrumentation before delegation, preserve the dirty worktree, and keep human review as the acceptance gate.

## Root Selection Within the Authorized Boundary

The selected real outcome is a review-ready implementation decision brief for Emmanuel and David that answers the unresolved July 14 operating question: what should be implemented next, where should work start, how should the bounded loop run, and what must remain held.

This is selected because the accepted EXP-02-R1 evidence defines the DDA optimization target and directs the next cycle toward a real outcome, while the July 14 meeting evidence explicitly asks for a specific implementation answer. The brief is the value-producing deliverable. EXP-03 contracts, ledgers, manifests, verifier returns, and scoreboards are evidence wrappers, not the outcome itself.

## Authorized Scope

- Read the frozen local source set named in the EXP-03 goal contract.
- Create review-only EXP-03 artifacts under `runs/2026-07-15/`.
- Delegate one bounded executor task after the goal, permissions, evidence rules, and instrumentation are frozen.
- Freeze the resulting candidate in a scoped local commit.
- Dispatch an independent verifier against that exact commit.
- Reconcile the result and present it for Emmanuel's human decision.

## Held Scope

No external write, push, runtime activation, automation, skill/eval or permanent-agent promotion, frontend, infrastructure, canon, PR, `main` promotion, repo replacement, or edit/commit of unrelated worktree files is authorized.

## Human Gate

The current instruction authorizes goal selection and execution within this boundary. It does not pre-accept the eventual candidate. Emmanuel retains the final `accept`, `revise`, `hold`, or `reject` decision after independent verification.
