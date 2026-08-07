# Weekly Huddle Cycle Protocol

## Cycle Contract

Each cycle converts bounded current context plus one weekly huddle into reviewed carry-forward state.

```text
Recover -> Prepare -> Meet -> Analyze -> Reconcile -> Review -> Route -> Carry Forward
```

## Stage 1: Recover

Inputs:
- `state/current-state.md`
- previous accepted action/decision register
- explicitly approved current project sources

Produce:
- current active goals
- active experiments
- open decisions
- holds/blockers
- previous commitments and status
- source gaps

Stop if the previous accepted state cannot be identified.

## Stage 2: Prepare

Create a `pre-huddle-packet.md` that contains:
- meeting objective
- changes since last cycle
- decisions needed
- experiments to inspect
- unresolved commitments
- bounded source list
- questions for David
- questions for Emmanuel

Keep the packet short enough to review before the meeting.

## Stage 3: Meet

The live huddle remains human-led.

The machine may supply context and questions, but it must not pre-decide the meeting outcome.

## Stage 4: Freeze Transcript

Record:
- target huddle date
- transcript path or durable URL
- source identity if available
- participant names
- any known transcript limitations

Historical transcripts may be used only when explicitly included as supporting context.

## Stage 5: Analyze

Preferred worker pattern when Firstmate orchestration is available:

### Scout A: Transcript Evidence
Extract:
- main themes
- explicit decisions
- proposals not yet approved
- actions
- owners
- blockers
- unresolved questions
- commitments
- supporting evidence or timestamps

### Scout B: Workflow Audit
Analyze:
- pre-huddle preparation quality
- context recovery burden
- duplicated work
- unclear authority
- source boundary problems
- workflow friction
- automation candidates
- work that must remain human-owned

Both scouts must label claims by evidence class.

If worker orchestration is unavailable, run the two passes manually and preserve their separation before reconciliation.

## Stage 6: Reconcile

Produce one `decision-action-register.md` and one `transcript-analysis.md`.

For each decision, record:
- decision
- evidence
- decision owner
- status
- downstream implication

For each action, record:
- action
- owner
- destination
- status
- source
- approval gate

Conflicts remain unresolved rather than being silently merged.

## Stage 7: Review and Route

Prepare `routing-return.md` with recommended destinations such as:
- GitHub
- Linear
- Notion
- Slack
- Codex implementation

Routing is a proposal until a human authorizes the write or execution.

## Stage 8: Carry Forward

Produce `next-huddle-state.md` containing only durable context needed next cycle:
- active goals
- active experiments
- open decisions
- holds
- active commitments
- David decisions needed
- Emmanuel actions
- next-huddle questions
- references to the completed run

After human review, this may replace `state/current-state.md`.

## Definition of a Completed Cycle

A cycle is complete when:
- source scope is explicit;
- transcript identity is explicit;
- decisions and proposals are separated;
- actions and owners are visible;
- unresolved questions remain visible;
- next-huddle state is prepared;
- any external routing or implementation is separately authorized.
