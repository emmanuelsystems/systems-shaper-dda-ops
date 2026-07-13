# Verifier Gate SOP v0.1

Status: `candidate_review_only`

The verifier gate records whether an artifact is accepted, held, rework, or rejected. It does not by itself make the artifact canon or runtime-ready.

## Verifier Result Shape

- Parent SHA:
- Reviewed SHA:
- Candidate SHA:
- Verifier result SHA, if committed:
- Review scope:
- Result: accepted / held / rework / rejected
- Burden score: low / medium / high / not measured
- Evidence example:
- Missing source, if any:
- Next owner:
- Next action:
- Proof boundary:
- Non-claims:

## Result Meanings

- `accepted`: The artifact satisfies the current review criteria.
- `held`: The artifact cannot advance because evidence, approval, or source clarity is incomplete.
- `rework`: The artifact needs changes before review can pass.
- `rejected`: The artifact should not advance in its current form.

## Runtime Boundary

Verifier acceptance is not runtime validation. Runtime-ready requires separate live evidence and validation.

## Independence Rule

The implementation return is not its own verifier result. The implementation owner freezes and returns one `candidate_sha`; a separate verifier reviews that exact SHA against `docs/review-only-acceptance-criteria.md` and records the result afterward.
