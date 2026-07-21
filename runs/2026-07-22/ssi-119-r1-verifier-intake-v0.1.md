---
title: SSI-119 R1 Correction Candidate Verifier Intake
asset_type: verifier_contract
status: held_until_post_commit_dispatch
version: v0.1
owner: Independent Verifier
created: 2026-07-22
goal_id: SSI-119-R1
parent_sha: ef539a2fb52439fb824f7f85072d0437b1275389
approval_status: not_accepted
---

# SSI-119 R1 Correction Candidate Verifier Intake

## Task

Independently review the immutable candidate identified by the post-commit dispatch envelope. Read committed Git objects only. Do not inspect a moving worktree as evidence, edit or repair the candidate, create reconciliation artifacts, or write externally.

## Required Inputs

- The immutable candidate SHA and candidate-bound links from the post-commit dispatch envelope.
- Exact parent commit [`ef539a2fb52439fb824f7f85072d0437b1275389`](https://github.com/emmanuelsystems/systems-shaper-dda-ops/commit/ef539a2fb52439fb824f7f85072d0437b1275389).
- The four files under `runs/2026-07-22/` named in the candidate allowlist.
- The parent-bound July 17 evidence named in the source index.

## Required Checks

### 1. Exact parent and changed-path allowlist

- Confirm the candidate has exactly one parent and it is `ef539a2fb52439fb824f7f85072d0437b1275389`.
- Confirm the candidate changes exactly the four allowed paths and no others.
- Confirm no July 17 artifact or CTR-01 frozen-candidate object was modified.

### 2. Manifest integrity

- Recompute SHA-256 from the exact candidate blobs for `source-index.md`, `ssi-119-r1-correction-candidate-v0.1.md`, and `ssi-119-r1-verifier-intake-v0.1.md`.
- Confirm all three values match `ssi-119-r1-candidate-manifest-v0.1.md`.
- Confirm the manifest correctly omits its own hash because embedding its final hash would be self-referential.

### 3. Immutable links and identity

- Confirm every GitHub blob URL in the candidate is bound to a full 40-character SHA.
- Confirm the only parent source URLs use `ef539a2fb52439fb824f7f85072d0437b1275389`.
- Confirm there are no moving branch URLs, fabricated candidate SHAs, or dispatch-token placeholders.
- Confirm the packet states that the post-commit dispatch envelope supplies the immutable candidate SHA and candidate-bound links.

### 4. Four-claim correction scope

Confirm the packet supersedes only these four claim defects:

1. requester and bounded execution authority were conflated;
2. report-limited `REWORK` evidence was presented as target-lineage independent verification;
3. lane descriptions did not enforce the strict serial lifecycle;
4. moving links and self-referential identity wording did not bind transport and review to immutable Git objects.

Confirm all other July 17 historical claims and artifacts remain preserved.

### 5. Reported CTR-01 defects

Confirm the packet preserves, without claiming repair, all five reported defect classes: stale fixture/wrong next action; incomplete fail-closed behavior; missing transition ownership; missing data classification/retention/persistence authority; and missing Slack/Linear coordination-only rule.

### 6. Serial lane checks

- Source recovery closed before the writer opened.
- Exactly one writer produced the allowlisted candidate.
- The writer closed at candidate freeze.
- Detached verification opened only after freeze.
- The verifier performed no repair, edit, recommit, or external write.

### 7. Separate CTR-01-R1 lineage conflict

Confirm the packet does not import or claim the later separate CTR-01-R1 lineage as evidence available at the exact parent. If any later CTR-01-R1 candidate or verifier return conflicts with the target-lineage recovery result, record the conflict separately; do not average it into, backfill, or silently upgrade this candidate's evidence status.

### 8. Held boundaries

Confirm SSI-119 is a correction of the July 17 decision packet, not a CTR-01 correction. Confirm CTR-01 correction remains held and the candidate does not authorize acceptance, CTR-01 implementation, live projections, data persistence, runtime, automation, frontend, memory, skill/eval or agent promotion, canon, infrastructure, PR, merge, `main`, push, external posting, or repository replacement.

## Verdict Vocabulary

Return exactly one verdict for correction completeness and decision-readiness: `accepted`, `held`, `rework`, or `rejected`.

An `accepted` verifier result means only that the exact frozen packet correctly states the four bounded corrections and proof limitations. It is not human acceptance, CTR-01 repair, implementation approval, runtime proof, or canon promotion.

## Return Shape

Return the exact candidate SHA reviewed, exact parent result, changed-path result, three manifest hash results, immutable-link and forbidden-token result, four-claim scope table, five reported-defect preservation table, serial-lane results, separate-lineage conflict note, held-boundary result, verdict, defects by severity, next owner, and next action.
