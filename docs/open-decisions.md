# Open Decisions

## Working Decisions For This Review Cycle

1. `systems-shaper-dda-ops` is the intended review surface for the manual DDA operating model, while remaining candidate and review-only infrastructure.
2. `dda-agent-ops` remains the active DDA pilot and evidence repo.
3. GitHub holds durable evidence. Slack and Linear coordinate status and decisions. Human approval controls promotion.
4. The July 13 rework return is implementation evidence only. An independent verifier reviews the frozen `candidate_sha` afterward.

These are bounded working decisions. They do not approve a PR, create or promote `main`, replace `dda-agent-ops`, or accept this repo as infrastructure.

## Decision Ownership

| Decision | Owner / gate |
|---|---|
| Frozen implementation candidate | Emmanuel returns the scoped `candidate_sha` |
| Independent result for review-only use | Independent verifier returns accepted / held / rework / rejected |
| Repo role beyond candidate review use | Emmanuel and David explicit human decision |
| PR, `main`, canon, or infrastructure promotion | Emmanuel and David explicit approval after review |
| Runtime-ready claim | Separate live validation and human approval |

## Still Open

1. Should this repo eventually own only workflow operations, or also agent source?
2. Should David use return branches by default after the bootstrap cycle?
3. Which reviewed artifacts may move from `runs/` into reusable `workflows/`?
4. When should workflow docs become reusable templates?
5. Should Linear / Symphony, Notion, or GitHub Issues own final project status after repo evidence is reviewed?
