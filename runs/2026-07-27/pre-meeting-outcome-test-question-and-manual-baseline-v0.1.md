---
title: Pre-Meeting Outcome Test Question and Manual Baseline
asset_type: test_input_freeze
status: question_and_baseline_frozen_execution_not_authorized
version: v0.1
owner: David Abiera
created: 2026-07-27
branch: codex/david-934fbd7-alignment-disposition-return-20260727
parent_sha: dee067ac9efcc01393af9f08877735008ac15841
test_id: PMOT-01
manual_baseline_id: PMB-2026-07-23
manual_baseline_sha: b1e8e4bd006a455aac45db54cb4d1a1dba9515b0
approval_scope: decision_question_and_manual_baseline_only
lane_authorization: none
experiment_status: not_started
runtime_claim: none
automation_claim: none
external_write_claim: scoped_branch_commit_and_push_only
---

# Pre-Meeting Outcome Test Question and Manual Baseline

## Frozen Decision Question

Using only verified current state, which single next DDA work item should David
and Emmanuel authorize:

1. one bounded real-world outcome run;
2. exact recovery and independent review of CTR-01-R1 objects
   `ed0410f6033462eff9046bb0f72957fdaf2ca4c4` and
   `ee379505cbcefb25f2a5fa9ec50dfcb6b1b37640`; or
3. creation of the missing contract-complete SSI-120 comparison artifact?

`HOLD` remains an allowed disposition if none of the three actions has adequate
evidence or authority.

For the selected result, the brief must name:

- the exact owner;
- the decision evidence;
- the required dependency;
- the first bounded action;
- the stop condition; and
- what remains explicitly unauthorized.

This question is frozen. Changing its three candidate actions or decision
standard requires a new human decision before any lane begins.

## Decision Standard

Select the action that provides the strongest near-term evidence that the DDA
can produce a useful outcome with less human recovery and coordination burden.

Do not select an action because it has the most existing documentation. Do not
select historical recovery unless the missing lineage blocks the chosen
real-world outcome. Do not select SSI-120 merely because its issue remains open.

## Manual Baseline Selection

Baseline: the July 23 human-directed pre-meeting preparation cycle ending at
exact commit
`b1e8e4bd006a455aac45db54cb4d1a1dba9515b0`.

Why this is the closest comparator:

- it prepared a document-first meeting walkthrough;
- it recovered GitHub, Slack, Linear, Calendar, and external-repository state;
- it attempted to make current decisions and holds visible;
- it used a human-steered preparation loop rather than the proposed bounded
  root, researcher, executor, and independent-verifier lanes; and
- it ended with a durable pre-meeting packet and coordination draft.

It is not a perfect comparator. The July 23 cycle covered more than one decision
and did not measure every burden field. Those limits remain part of the
baseline.

## Frozen Baseline Window

| Boundary | Evidence |
|---|---|
| Start | Read-only recovery at approximately `2026-07-23 07:14 Asia/Shanghai`, recorded in the exact source index |
| Intermediate checkpoint | Slack checkpoint at `2026-07-23 07:34:03 Asia/Shanghai` |
| Human redirection | David reply at `2026-07-23 08:05:47 Asia/Shanghai` requesting four remaining field groups |
| End | Commit `b1e8e4bd` at `2026-07-23 08:14:28 Asia/Shanghai` |
| Approximate elapsed preparation time | `60 minutes` |

The start time is approximate. The elapsed value must therefore be reported as
approximate, not exact.

## Frozen Baseline Scorecard

| Measure | Baseline value | Evidence boundary |
|---|---:|---|
| Decision breadth | 5 decision rows plus unresolved meeting logistics | Exact `david-meeting-start-here-v0.1.md` |
| Durable source entries | 16 | Exact July 23 source-index table |
| Listed preparation artifacts | 10 | Exact July 23 artifact-set table |
| Approximate elapsed preparation time | 60 minutes | Approximate recovery start to exact final commit time |
| Documented mid-cycle human redirections | At least 1 | David's exact Slack reply requested four remaining field groups |
| External coordination writes | 1 sent Slack checkpoint | Exact source index and update summary |
| Additional Slack draft | 1, not sent | Exact `b1e8e4bd` commit |
| Independent verification of the pre-meeting packet | None | July 23 hold states earlier verifier results did not verify the prep packet |
| Human disposition reached during the cycle | No | SSI-119 disposition remained pending |
| Meeting logistics resolved | No | Status remained `unconfirmed` |
| Material-claim evidence coverage | Unknown | No numeric percentage was recorded |
| Source-recovery time alone | Unknown | Only the total preparation window can be approximated |
| Token or cost burden | Unknown | Not recorded |
| Verifier defect count for the prep packet | Unknown / not applicable | No independent prep-packet verifier ran |
| Decision time using the brief | Unknown | No completed human decision was recorded in the cycle |

`Unknown` values must not be converted into zero, pass, or failure.

## Prospective Comparison Rules

The first real-world test must use the same definitions below.

| Measure | Prospective rule |
|---|---|
| Decision breadth | One frozen decision question; three candidate actions; `HOLD` permitted |
| Preparation elapsed time | Start when authorized source recovery begins; stop when the brief candidate is frozen |
| Human redirection | Count any human correction caused by missing scope, wrong source, unsupported claim, or changed task routing after freeze |
| Artifact burden | Count every durable test artifact; do not hide lane returns |
| Source burden | Count every material source opened and every failed recovery |
| Evidence coverage | Material claims with an exact source or explicit `UNKNOWN`, divided by all material claims |
| Independent verification | Required on one frozen candidate; verifier may not repair it |
| Decision time | Start when David opens the verified brief; stop at `accept`, `hold`, `rework`, or `reject` |
| External writes | Count separately; none is required during preparation |

## Material-Improvement Gate

Quality gates:

1. one decision question remains stable;
2. every material claim is sourced or marked `UNKNOWN`;
3. no unresolved critical verifier defect exists;
4. David's decision boundary remains human-owned; and
5. no unauthorized external or runtime action occurs.

The test may claim material improvement only if all quality gates pass and at
least three of these five baseline comparisons improve:

1. a human disposition is reached, versus none in the baseline;
2. an independent verifier reviews the prep packet, versus none;
3. elapsed preparation is below approximately 60 minutes;
4. no mid-cycle human redirection is required after the question is frozen; and
5. the durable preparation artifact count is five or fewer, versus ten.

If the result passes quality gates but improves fewer than three comparison
measures, classify it `useful_but_not_materially_improved`.

## Stop Conditions Before Lane Authorization

Do not authorize lanes if:

- the exact decision question is disputed;
- the July 23 cycle is rejected as the manual comparator;
- the source and artifact counting rules are not accepted;
- the required human decision window cannot be observed; or
- the test would require an external write or runtime change to produce the
  brief.

## Current Authorization

Authorized now:

- freeze this exact question;
- freeze the manual baseline and comparison rules; and
- commit and push this record on the scoped David review branch.

Not authorized:

- create or dispatch root, researcher, executor, or verifier lanes;
- start source recovery for the prospective test;
- draft the prospective meeting brief;
- publish historical objects;
- create SSI-120;
- write Slack or Linear;
- execute runtime, provider, automation, memory, skill, eval, PR, merge, or
  `main` actions.
