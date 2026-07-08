# Codex Operating Rules

This repo is a review-only workspace for Systems Shaper DDA / Codex operations. Codex should preserve proof boundaries and treat human review as the acceptance gate.

## Codex May

- Read markdown files.
- Create draft markdown files.
- Build repo scaffolds.
- Draft workflow docs.
- Draft templates.
- Produce completion packets.
- Check consistency across files.

## Codex Must Not

- Treat raw chat as durable truth.
- Assume external integrations exist.
- Enable automations.
- Save memory.
- Promote skills or evals.
- Change source-of-truth rules without approval.
- Treat its own output as final.
- Push directly to `main` without approval.

## Read Order

1. `README.md`
2. `docs/source-of-truth.md`
3. `docs/source-authority-ladder.md`
4. Current `runs/YYYY-MM-DD/source-index.md`
5. Relevant workflow or template files

## Write Targets

Codex should write new work into dated `runs/YYYY-MM-DD/` folders first unless the user explicitly asks for a workflow, template, docs, schema, or reference update.

## Team Update SOP

Use this repo as the durable update ledger for Systems Shaper DDA / Codex operations. Every meaningful work cycle should start in a dated `runs/YYYY-MM-DD/` folder before outward reporting or promotion.

The dated run folder must follow the date the update is pushed or materially updated. If an older packet is corrected, reconciled, or pushed on a later day, create or update that later day's `runs/YYYY-MM-DD/` ledger and point back to the original artifact instead of silently treating the older dated folder as the whole update record.

For each work cycle, create or update:

- `source-index.md`
- a DDA -> Codex handoff packet when execution is requested
- a Codex -> DDA completion packet when Codex returns work
- an update summary when a pushed or material update affects older run-folder artifacts
- a verifier return when review is needed
- a status/update summary only when useful for reporting

The default update loop is:

```text
Human intent
->
DDA / ChatGPT source-indexes the ask
->
Codex or David works on a scoped branch
->
Completion or return packet is added
->
Verifier result is added
->
Status becomes accepted / held / rework / rejected
->
Only reviewed material can be considered for promotion
```

## Branch Use

- Emmanuel setup work: `codex/emmanuel-<task>-YYYYMMDD`
- David return work: `codex/david-<task>-return-YYYYMMDD`
- Codex execution work: `codex/<task>-YYYYMMDD`
- Human review before promotion: `review/<artifact-or-workflow>-v0-1`
- `main`: reviewed durable source only

David-side return branches should include what changed, what source was used, what is accepted / held / rework / rejected, what is missing, and the recommended next owner/action.

Emmanuel-side setup branches should include the ask, source anchors, what not to claim, the requested return shape, and the current proof boundary.

## Reporting Rule

Update the repo first. Slack, Notion, Linear, Symphony, Drive, and other external surfaces should receive only approved summaries, and only when the user explicitly asks for that external update.

No important DDA / Codex update should be treated as durable until it has a dated source index, scoped branch, completion or return packet, and verifier result or explicit hold note.

When reporting a pushed update, cite the run folder for the push/update date and include the original artifact paths if they live under an earlier date.

## Approval Boundaries

Drafts may become candidate artifacts after a repo-local consistency check. Candidate artifacts may become accepted only after human review. Accepted artifacts do not become canon or runtime-ready without separate approval and validation.

## Commit Expectations

Use scoped branches for all changes. Do not commit unrelated edits. Do not merge or push directly to `main`. A commit preserves review evidence; it does not create acceptance.
