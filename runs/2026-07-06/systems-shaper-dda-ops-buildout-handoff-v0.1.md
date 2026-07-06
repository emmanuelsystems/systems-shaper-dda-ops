# DDA -> Codex Handoff Packet

## Repo Buildout: `systems-shaper-dda-ops`

## 1. Task Summary

- Task: Build out the initial GitHub repo structure for `systems-shaper-dda-ops` and prepare the first set of review-only markdown files.
- Why this matters: Test whether a dedicated Systems Shaper DDA operations repo can become the cleaner long-term home for the David / Emmanuel / Codex push-pull workflow, separate from the current `dda-agent-ops` pilot repo.
- Desired outcome: Create a clean initial repo scaffold with source-of-truth rules, branch strategy, workflow docs, templates, run folder structure, and proof-boundary notes so David and Emmanuel can review whether this repo should become the long-term DDA / Codex operations workspace.

## 2. Context

- Current active repo: `emmanuelsystems/dda-agent-ops`
- Proposed new repo: `emmanuelsystems/systems-shaper-dda-ops`
- Important boundary: Do not treat `systems-shaper-dda-ops` as accepted infrastructure yet.
- Working thesis: The current `dda-agent-ops` repo is good for the DDA pilot, but a dedicated `systems-shaper-dda-ops` repo may be better for broader team workflow structure.

## 3. Scope

## In Scope

- Create or prepare the initial repo scaffold for `systems-shaper-dda-ops`.
- Add initial markdown files.
- Add clear source-of-truth and proof-boundary docs.
- Add initial branch strategy documentation.
- Add Codex handoff and completion templates.
- Add verifier return template.
- Add today's initial run folder.
- Add a repo bootstrap summary.
- Prepare the first commit and push if the repo exists and credentials/remote are available.
- If the repo does not exist yet, prepare the full local scaffold and return exact creation/push instructions.

## Out of Scope

- Do not delete or replace `dda-agent-ops`.
- Do not migrate historical artifacts automatically.
- Do not claim this repo is canon.
- Do not claim this repo is accepted infrastructure.
- Do not claim this repo is Context Vault.
- Do not enable automation.
- Do not save memory.
- Do not create or promote skills.
- Do not create or promote evals.
- Do not update Slack, Notion, Linear, Symphony, Drive, or memory.
- Do not merge anything into `main` or `master` without explicit human approval.

## Do Not Change

- Do not modify `emmanuelsystems/dda-agent-ops` unless explicitly instructed.
- Do not overwrite approved source-of-truth rules.
- Do not treat raw chat or Slack history as durable truth unless captured in reviewed markdown.
- Do not assume David has approved the new repo.
- Do not assume this repo should replace the current pilot repo.

## 4. Requested Codex Work

- Work type: Repo bootstrap plus initial markdown source files.
- Primary task: Build the initial `systems-shaper-dda-ops` repo scaffold.
- Preferred branch: `codex/bootstrap-systems-shaper-dda-ops-20260706`
- Default branch boundary: Use `main` unless the repo already exists with a different default branch, but do not work directly on `main`.

## 5. Acceptance Criteria

- The initial file scaffold exists.
- The bootstrap branch exists locally.
- The initial markdown files are populated with useful review-only content.
- `git status --short --branch` is checked.
- A commit is created if safe.
- A push is attempted only if the remote exists and credentials are available.
- If push is blocked, report the blocker and exact next command.
- The completion packet lists all files created.
- The completion packet preserves proof boundaries and non-claims.

## 6. Evidence Required

- Local path used.
- Repo remote status.
- Branch name.
- Files created.
- Git status before commit.
- Git status after commit.
- Commit hash if created.
- Push status.
- Blocker if push failed.
- Exact next command if human action is needed.

## 7. Open Questions to Preserve

- Should `systems-shaper-dda-ops` become the long-term DDA / Codex operations repo?
- Should `dda-agent-ops` remain the DDA pilot repo?
- Should this new repo sit above `dda-agent-ops` rather than replace it?
- Who approves promotion into `main`?
- Should David always use return branches?
- Should `codex/dda-ops-evidence-packet` become the default shared evidence branch?
- Should Linear / Symphony or Notion own final project status?
- When do workflow docs move from `runs/` into `workflows/`?
- What is the exact review gate before any reusable workflow becomes canon?
