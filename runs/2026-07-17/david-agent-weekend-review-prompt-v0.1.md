---
title: David Agent Weekend Detached Review Prompt
asset_type: verifier_prompt
status: prepared_pending_exact_sha_dispatch
version: v0.1
owner: Emmanuel Olana
created: 2026-07-17
candidate_sha: supplied_at_dispatch
external_write_claim: none
---

# David Agent Weekend Detached Review Prompt

Use this as a thin prompt with the frozen July 17 packet as the thick context.

## Prompt

Review the exact commit supplied by Emmanuel on branch `codex/emmanuel-weekend-decision-closure-20260717` in `emmanuelsystems/systems-shaper-dda-ops`.

Read committed Git objects only. Start with:

1. `runs/2026-07-17/source-index.md`
2. `runs/2026-07-17/decision-closure-candidate-v0.1.md`
3. `runs/2026-07-17/real-outcome-preflight-v0.1.md`
4. `runs/2026-07-17/conversation-lane-disposition-v0.1.md`
5. `runs/2026-07-17/eod-progress-report-v0.1.md`

Then inspect only the exact prior SHAs and Slack links named by the source index when needed.

Determine whether the packet completely and consistently answers David's July 17 request:

1. EXP-03 disposition, outcome classification, rationale, and next owner/action.
2. CTR-01 disposition and the conditions required before any correction.
3. First real-outcome classification, acceptance evidence, burden measures, and launch gates.
4. Conversation lanes to keep, use conditionally, make dormant, archive, or prohibit.
5. Exact branch, parent, candidate SHA, changed-path scope, held boundaries, and next gate.

Challenge the recommendations. Do not accept the packet's framing by default.

Test specifically for:

- accidental conversion of EXP-03 decision-readiness into a real-outcome baseline claim;
- loss or rewriting of the CTR-01 `REWORK` evidence;
- hidden authorization of a CTR-01 correction or another experiment;
- plan completeness being substituted for operational value;
- missing data, retention, persistence, or source-authority decisions;
- duplicated lanes, parallel writers, child dispatch, or self-verification;
- unsupported repeatability, improvement, automation, runtime, canon, or architecture claims;
- any mismatch between the source index, decision packet, preflight, lane record, and EOD.

Do not edit the candidate, create a correction, post externally, start the Monday outcome, or authorize held work.

Return:

- exact candidate SHA reviewed;
- manifest/scope check;
- verdict: `accepted`, `rework`, `held`, or `rejected` for completeness and decision-readiness only;
- criteria table with pass/fail and exact evidence anchors;
- contradictions, omissions, and defects by severity;
- whether each recommended decision is supported, unsupported, or requires human judgment;
- required corrections before David review;
- next owner and action;
- proof limitations and remaining holds.

An `accepted` result means only that the packet is complete and decision-ready for David and Emmanuel. It does not accept the decisions, launch the real outcome, authorize CTR-01 correction, or establish runtime readiness.
