# Source Authority Ladder

Use the highest available source when making a claim. Do not confuse the order used to find evidence with the authority of that evidence.

## Claim Authority Order

1. Human review decision or independent verifier return anchored to an exact `candidate_sha` and stated scope.
2. Reviewed repo artifact at the exact `reviewed_sha` named by that decision.
3. Current dated run source index anchored to the relevant parent, reviewed, and candidate SHA context.
4. Linked issue or task with an explicit human-set status.
5. Approved Notion or planning artifact.
6. Drive source document or transcript.
7. Slack coordination thread.
8. ChatGPT / DDA working context.
9. Unverified memory or recollection.

An independent verifier return can accept an artifact only for its stated review scope. It does not create canon, runtime validation, or infrastructure approval.

## Navigation Order

A fresh reviewer should start with the latest dated source index because it routes to the relevant evidence. The reviewer should then inspect the exact commit and artifact, followed by the independent verifier return when one exists. Starting with a source does not make it the highest authority.

## SHA Rule

- `parent_sha`: the commit immediately before the scoped implementation pass.
- `reviewed_sha`: the frozen commit the review or rework request evaluated.
- `candidate_sha`: the frozen implementation commit returned for independent review.
- `verifier_result_sha`: the later commit that records the independent verifier result, if the result is committed.

A commit cannot contain its own final hash. The implementation return records the exact parent and reviewed SHAs; the returned Git commit is the `candidate_sha`. The independent verifier packet must then name that exact `candidate_sha`.

## Conflict Rule

When sources conflict, Codex should name the conflict instead of averaging the claims.

## Missing Evidence Rule

When a source is unavailable, name the unavailable source and keep the claim held. Do not silently upgrade working context into durable truth.
