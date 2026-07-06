# Systems Shaper DDA Ops

This repo is a review-only operations workspace for Systems Shaper DDA / Codex workflows.

It is intended to test and document how Emmanuel, David, DDA / ChatGPT, and Codex coordinate repo-backed work through source-indexed run folders, handoff packets, completion packets, verifier gates, and human review.

## Current Status

Status: `bootstrap_review_only`

This repo is not accepted infrastructure yet.

It does not replace `dda-agent-ops` unless explicitly approved by Emmanuel and David.

## Core Rule

DDA owns daily alignment.
Codex owns repo-local execution.
GitHub owns durable markdown evidence.
Slack owns coordination signals.
Notion / Linear / Symphony own planning and status only when explicitly used.
Human review decides accepted / held / rework / rejected.

## Source-of-Truth Summary

Durable source lives in reviewed markdown artifacts and Git history. Daily context, chat history, Slack messages, and memory can help orient work, but they are not durable truth until captured in a reviewed repo artifact.

## Branch Model Summary

`main` is reserved for reviewed durable source. Bootstrap, workflow setup, migration planning, and return work should happen on scoped branches and remain review-only until approved.

## Human Approval Rules

Commit and push are transport steps only. They do not mean an artifact is accepted, canon, validated, runtime-ready, or approved infrastructure.

## Proof Boundary

No automation.
No memory save.
No skill promotion.
No eval promotion.
No Context Vault claim.
No runtime validation claim.
No accepted-infrastructure claim.
