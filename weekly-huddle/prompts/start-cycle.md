# Prompt: Start Weekly Huddle Cycle

Use this prompt to initialize a new weekly huddle run.

```text
Start a new Weekly Huddle Machine cycle.

Run date:
<CURRENT RUN DATE>

Target huddle date:
<TARGET HUDDLE DATE>

Use:
- weekly-huddle/README.md
- weekly-huddle/AGENTS.md
- weekly-huddle/protocols/cycle.md
- weekly-huddle/state/current-state.md

Objective:
Recover the smallest useful current state and prepare a bounded pre-huddle packet for Emmanuel and David.

Create a new folder:
weekly-huddle/runs/<RUN DATE>/

Create:
- source-index.md
- state-snapshot.md
- pre-huddle-packet.md

Requirements:
- distinguish current state from historical context;
- identify missing evidence instead of filling gaps;
- separate David decisions from Emmanuel actions;
- surface active goals, experiments, holds, commitments, and unresolved questions;
- keep the prep packet reviewable in under 10 minutes;
- do not implement, route externally, merge, or change persistent state.

At completion, report the exact files created and the source boundary used.
```
