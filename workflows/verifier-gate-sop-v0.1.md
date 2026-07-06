# Verifier Gate SOP v0.1

Status: `candidate_review_only`

The verifier gate records whether an artifact is accepted, held, rework, or rejected. It does not by itself make the artifact canon or runtime-ready.

## Verifier Result Shape

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
