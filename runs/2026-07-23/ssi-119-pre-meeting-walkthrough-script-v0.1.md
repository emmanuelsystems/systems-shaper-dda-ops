---
title: SSI-119 Pre-Meeting Walkthrough Script
asset_type: meeting_script
status: review_ready_meeting_unconfirmed
version: v0.1
owner: Emmanuel Olana
created: 2026-07-23
approval_status: pending_human_review
external_write_claim: none
---

# SSI-119 Pre-Meeting Walkthrough Script

## Before the Call

Open one document first, then use the remaining links only as supporting evidence:

1. [David meeting start-here walkthrough](david-meeting-start-here-v0.1.md)
2. [David's July 21 direction](https://systemsshaperinc.slack.com/archives/C073QL4CFC4/p1784583652642079?thread_ts=1784538966.012259&cid=C073QL4CFC4)
3. [Frozen SSI-119 candidate](https://github.com/emmanuelsystems/systems-shaper-dda-ops/commit/2fb4f621998b2af5fd8f51da35bba159d484e767)
4. [Detached verifier result](https://github.com/emmanuelsystems/systems-shaper-dda-ops/blob/9aa111f597c9adeda29f04eb6c094e04dd286995/runs/2026-07-22/ssi-119-r1-verifier-return-v0.1.md)
5. [Completion return](https://github.com/emmanuelsystems/systems-shaper-dda-ops/blob/b4d4aa8c48b05da6bc141ec6a940f3483bfa4707/runs/2026-07-22/codex-to-dda-ssi-119-r1-completion-v0.1.md)

Do not reproduce transcript content. Use the start-here document for status, corrections, limitations, SSI-120 facts versus inference, decisions, and next action.

Do not start the walkthrough until David confirms the date, time, location/link, and recording plan.

## 0:00-2:00 — Logistics and Boundary

Say:

> Before we start, I need to confirm that this is the intended huddle, the location/link is correct, and the recording plan is agreed. I am starting the recording now. I will verify the visible recording indicator before we discuss the packet.

Manually verify the recording indicator. If it is absent, stop substantive discussion until recording is active or both participants explicitly agree to proceed without it.

Then say:

> This is a review and disposition meeting. It does not authorize CTR-01 implementation, SSI-120 architecture, replay, runtime work, promotion, or canon. GitHub transport and verifier acceptance are not human acceptance.

## 2:00-7:00 — SSI-119 Identity and Status

Show the exact candidate commit and say:

> My delivery classification is partial. The bounded R1 artifact and detached verification are complete, but the issue is not closed because human disposition and Linear reconciliation remain incomplete.
>
> The direct parent is `ef539a2fb52439fb824f7f85072d0437b1275389`. The frozen candidate is `2fb4f621998b2af5fd8f51da35bba159d484e767`. It adds exactly four July 22 paths. The detached verifier result is `9aa111f597c9adeda29f04eb6c094e04dd286995` and accepts correction completeness and decision-readiness only. Both branches are now remotely reachable. SSI-119 still shows Todo in Linear.

Pause for identity objections. Resolve SHA or path disputes before continuing.

## 7:00-12:00 — Four Corrections

Say:

> The decision is limited to four corrections.

1. Request attribution: David requested the July 17 return; Emmanuel separately authorized bounded execution and transport.
2. Evidence status: the target lineage reports CTR-01 `REWORK`, but the underlying verifier artifact is absent there, so the claim is source-recovered and report-limited.
3. Lane lifecycle: source recovery closes before one writer opens; the writer closes at freeze; detached verification starts after freeze and cannot repair the candidate.
4. Immutable identity: exact-parent evidence and review links use full Git SHAs; the candidate cannot embed its own final SHA.

Then ask:

> Do you find a defect in any of these four corrections, or can we disposition the exact candidate as accept, hold, rework, or reject?

## 12:00-17:00 — Separate CTR-01-R1 Lineage

Say:

> A separate local lineage has CTR-01-R1 candidate `ed0410f6033462eff9046bb0f72957fdaf2ca4c4` and verifier result `ee379505cbcefb25f2a5fa9ec50dfcb6b1b37640`, accepted for design decision-readiness only. It is not an ancestor of the SSI-119 target parent, was not imported, and cannot backfill the missing target-lineage verifier artifact. It grants no implementation authority.

Ask for one treatment only: recognize it for later design review, hold for provenance reconciliation, or exclude it from this packet.

## 17:00-22:00 — SSI-120 Research Boundary

Say:

> SSI-120 is partial. We have source-backed Graphify observations and context-only records for the remaining shares, but not the required concise comparison of the exact orchestrator repository and Karpathy LLM Council project. Graphify may reduce orientation burden; that is a hypothesis, not a result. No architecture or test is authorized here.

Ask whether the next output is the exact comparison note or an explicit hold.

## 22:00-27:00 — Record Decisions

Complete this table live:

| Decision | Allowed values | Recorded result |
|---|---|---|
| SSI-119 four-correction disposition | accept / hold / rework / reject | |
| External reconciliation | authorize named surfaces / withhold | |
| CTR-01-R1 treatment | later design review / provenance hold / exclude | |
| SSI-120 next output | comparison note / hold | |
| Replay | remain not_started / define later gate | |

For any `rework`, record the exact defect, owner, evidence required, and return time. For any external write authorization, name the exact surface. Do not infer blanket authority.

## 27:00-30:00 — Baton Pass

Say:

> I will read back the baton pass as owner, output, timing, dependency, evidence, and stop condition. Anything not explicitly assigned remains held.

Read back each decision. Confirm where the decision record will live. End with:

> No additional implementation begins from this meeting unless a separate action is explicitly authorized and recorded.

## Stop Conditions

Stop the workflow if:

- meeting logistics remain unconfirmed;
- the recording indicator cannot be verified and no explicit agreement to proceed exists;
- the candidate SHA or changed-path set is disputed;
- a decision would collapse SSI-119 correction into CTR-01 implementation or SSI-120 architecture;
- the requested external write surface is not named;
- no owner, evidence requirement, or next timing can be recorded.
