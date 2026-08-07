# Prompt: Process Weekly Huddle Transcript

Use this prompt after a weekly huddle transcript is available.

```text
Process this Weekly Huddle Machine cycle.

Run date:
<CURRENT RUN DATE>

Target huddle date:
<TARGET HUDDLE DATE>

Primary transcript:
<EXACT PATH OR DURABLE URL>

Use:
- weekly-huddle/README.md
- weekly-huddle/AGENTS.md
- weekly-huddle/protocols/cycle.md
- weekly-huddle/state/current-state.md
- weekly-huddle/runs/<RUN DATE>/source-index.md
- weekly-huddle/runs/<RUN DATE>/pre-huddle-packet.md

If Firstmate worker dispatch is verified, use exactly two read-only scouts:
1. Transcript Evidence Scout
2. Workflow Audit Scout

If Firstmate dispatch is unavailable, perform two clearly separated analysis passes before reconciliation.

Produce:
- transcript-analysis.md
- decision-action-register.md
- routing-return.md
- next-huddle-state.md

Requirements:
- treat the named transcript as primary evidence;
- do not substitute another transcript if it is unavailable;
- separate confirmed decisions from proposals;
- record owners for actions or mark them unassigned;
- preserve unresolved conflicts;
- distinguish direct evidence, interpretation, recommendation, unresolved decision, and missing evidence;
- routing is proposal-only unless separately authorized;
- do not overwrite weekly-huddle/state/current-state.md;
- do not implement recommendations;
- do not merge or write externally.

At completion, report:
- exact primary source used;
- files created;
- unresolved decisions;
- whether the cycle meets the completion criteria in protocols/cycle.md.
```
