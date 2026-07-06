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

## Main Rule

Do not push directly to `main` without explicit human approval. Do not treat branch creation, commit, or push as acceptance.
