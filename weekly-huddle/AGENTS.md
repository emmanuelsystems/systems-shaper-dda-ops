# Weekly Huddle Machine Operating Rules

This folder defines a reusable, review-only weekly huddle operating machine for Emmanuel and David.

## Read Order

1. `README.md`
2. `protocols/cycle.md`
3. `state/current-state.md`
4. Current run `runs/YYYY-MM-DD/source-index.md`
5. Relevant templates or prompts

## Allowed

- Read approved source material.
- Create or update draft markdown artifacts for the current run.
- Recover state from accepted prior artifacts.
- Extract direct transcript evidence.
- Compare multiple bounded analyses.
- Produce recommendations clearly labeled as recommendations.
- Prepare routing proposals for human review.

## Not Allowed

- Treat a transcript summary as a human decision unless the transcript supports it.
- Treat a Git branch or commit as approval.
- Promote recommendations into accepted actions without review.
- Write to Slack, Linear, Notion, Drive, or other external systems unless explicitly authorized.
- Start Codex implementation work unless Emmanuel approves a bounded handoff.
- Merge, rebase, or close holds without explicit approval.
- Save raw transcript history as default persistent memory.
- Claim Firstmate orchestration succeeded unless worker dispatch and reconciliation actually completed.

## Evidence Labels

Every important statement should be classifiable as one of:

- `direct_evidence`
- `evidence_backed_interpretation`
- `recommendation`
- `unresolved_decision`
- `missing_evidence`

## Run Rule

Each huddle cycle gets its own folder under `weekly-huddle/runs/YYYY-MM-DD/`.

The run date is the date the machine is executed, not necessarily the meeting date. Every run must explicitly record the target huddle date.

## State Rule

Only reviewed carry-forward context belongs in `state/current-state.md`.

A new transcript does not directly overwrite persistent state. The post-huddle reconciliation must first produce a candidate `next-huddle-state.md`, which is reviewed before promotion into `state/current-state.md`.

## Human Gates

- Emmanuel confirms source scope and execution readiness.
- David confirms decisions or receiving-side intent where required.
- Joint approval is required for changes that alter the machine's governance, canonical source rules, or automation authority.
