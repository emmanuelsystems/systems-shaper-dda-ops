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

## Approval Boundaries

Drafts may become candidate artifacts after a repo-local consistency check. Candidate artifacts may become accepted only after human review. Accepted artifacts do not become canon or runtime-ready without separate approval and validation.

## Commit Expectations

Use scoped branches for all changes. Do not commit unrelated edits. Do not merge or push directly to `main`. A commit preserves review evidence; it does not create acceptance.
