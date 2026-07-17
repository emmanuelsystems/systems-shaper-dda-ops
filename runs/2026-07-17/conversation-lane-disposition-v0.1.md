---
title: Conversation Lane Disposition
asset_type: lane_disposition_record
status: proposed_pending_human_review
version: v0.1
owner: Root Orchestrator
created: 2026-07-17
---

# Conversation Lane Disposition

## Decision Rule

Keep a lane only when it contributes unique evidence, execution, verification, or reconciliation to one approved goal. Packet count and conversation count are not value measures.

## Disposition

| Lane | Evidence from current cycles | Disposition | Rule |
|---|---|---|---|
| Root orchestrator | Preserved goal lineage, reconciled returns, froze candidates, and retained human gates | `keep` | Sole planning, routing, reconciliation, and final recommendation authority below the human gate |
| Bounded executor / plan writer | Produced the EXP-03 decision brief and explicit evidence return | `keep_one_when_needed` | One writer only; no parallel writers against the same candidate |
| Detached verifier | Caught EXP-02 defects and bounded later acceptance; EXP-03 review preserved scope | `keep_required` | Read-only review after exact freeze; may not repair its candidate |
| Researcher / source recovery | Useful only when a named source gap exists | `conditional_dormant` | Activate at most one read-only lane with a frozen question and source set |
| Advisor / critique lane | Can surface risks but overlaps root and verifier when no distinct question exists | `dormant` | Activate only for a named pre-freeze judgment not covered by the verifier |
| Multiple general analysis conversations | Duplicate context recovery and increase reconciliation burden | `archive_after_capture` | Capture unique evidence first; then archive or leave dormant |
| Child or dynamic dispatch | No demonstrated need in the current bounded loop | `prohibited_for_v1` | Root dispatches only from the frozen dispatch set |
| Parallel writers | Creates merge and authority ambiguity | `prohibited_for_v1` | One bounded writer owns the candidate output |

## V1 Weekend Control

- One root orchestrator.
- At most two specialist lanes active at once.
- Source-recovery lane is read-only.
- One writer maximum.
- Detached verifier starts only after candidate freeze.
- No child or dynamic dispatch.
- Final decision remains human-owned.

## Archive Condition

A conversation can become dormant or archived after its unique source, decision, return, or unresolved hold is captured in the dated run folder. Archiving does not delete the historical evidence.

## Proof Boundary

This is a proposed lane disposition for the weekend packet, not a permanent agent taxonomy or approved orchestration architecture.
