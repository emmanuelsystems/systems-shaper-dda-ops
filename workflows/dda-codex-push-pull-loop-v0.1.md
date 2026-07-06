# DDA / Codex Push-Pull Loop v0.1

Status: `candidate_review_only`

This workflow describes a proposed loop. It is not canon and is not runtime-ready.

## Loop

```text
Human intent
->
DDA / ChatGPT source-indexes and creates handoff
->
Codex pulls repo and reads source authority files
->
Codex drafts changes on a branch
->
Codex returns completion packet
->
Human verifier reviews result
->
Status becomes accepted / held / rework / rejected
->
Reviewed artifact may be promoted
->
Slack / Linear / Notion receive status only after approval
```

## Required Gates

- Source-index before execution.
- Branch before repo edits.
- Completion packet before outward reporting.
- Human verifier before acceptance.
- Separate validation before runtime-ready claims.

## Non-Claims

This loop does not enable automation, save memory, promote evals, promote skills, or make this repo accepted infrastructure.
