# Branch and Return SOP v0.1

Status: `candidate_review_only`

This branch model is proposed for review. It does not replace existing branch rules unless approved.

## Branch Model

```text
main
  reviewed durable source only

codex/dda-ops-evidence-packet
  shared review-only evidence branch

codex/bootstrap-systems-shaper-dda-ops-YYYYMMDD
  bootstrap branch

codex/import-dda-agent-ops-evidence-YYYYMMDD
  migration planning branch

codex/workflow-setup-YYYYMMDD
  workflow setup branch

codex/david-<task>-return-YYYYMMDD
  David-side return branch

codex/emmanuel-<task>-YYYYMMDD
  Emmanuel-side setup branch

review/<artifact-or-workflow>-v0-1
  human review branch before promotion
```

## Return Rule

Return branches should include a completion packet, source index, and verifier-ready summary before any merge or promotion discussion.

For a rework pass, freeze one implementation commit and return:

- `parent_sha`,
- `reviewed_sha`,
- the frozen commit as `candidate_sha`,
- dated run folder,
- complete changed-file manifest,
- implementation summary,
- remaining holds.

The implementation owner must not provide the independent verifier result for the same rework. The independent verifier reviews the frozen `candidate_sha` afterward and records that SHA in the verifier return.

## Bootstrap And Default-Branch Posture

The current bootstrap work stays on `codex/bootstrap-systems-shaper-dda-ops-20260706`. The configured remote HEAD may point to this bootstrap branch while the repo has no approved `main`; that is a transport and discoverability posture only.

Do not create, promote, or push `main`, and do not open a PR, without explicit Emmanuel and David approval. A later approved default-branch decision must be recorded as a separate human decision and must not be inferred from the remote HEAD setting.

## Main Rule

Do not push directly to `main` without explicit human approval. Do not treat branch creation, commit, or push as acceptance.
