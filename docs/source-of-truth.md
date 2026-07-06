# Source of Truth

This repo separates orientation context from durable truth. Repo artifacts become durable only when reviewed, committed, and kept within the correct proof boundary.

## Ownership Model

| Surface | Owns |
|---|---|
| GitHub | Durable markdown evidence, workflows, templates, version history |
| DDA / ChatGPT | Daily alignment, reasoning, handoff drafting, synthesis |
| Codex | Repo-local execution, drafting, refactoring, verification |
| Slack | Coordination signals and team-safe updates |
| Drive | Source documents, transcripts, shareable docs |
| Notion | Human-readable planning, dashboards, rough notes |
| Linear / Symphony | Project tracking, gates, review status |
| Human review | Accepted / held / rework / rejected decisions |

## Rules

- Chat history is temporary context only.
- Slack history is coordination context only unless captured in reviewed markdown.
- Codex output becomes durable only after human review and commit.
- GitHub commit/push is transport, not acceptance.
- Human approval is required before treating anything as final.
- When evidence is incomplete, use held, rework, Yellow, validation hold, or not yet proven language.

## Non-Claims

This repo does not prove automation, runtime readiness, skill promotion, eval promotion, Context Vault status, or accepted infrastructure status.
