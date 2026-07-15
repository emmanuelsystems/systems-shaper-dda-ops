---
title: EXP-02-R1 Candidate Manifest
asset_type: candidate_manifest
status: ready_for_candidate_commit
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: EXP-02-PM2E-2026-07-15
iteration_id: EXP-02-R1
candidate_sha: assigned_by_commit_containing_this_manifest
---

# EXP-02-R1 Candidate Manifest

## Freeze Rule

The Git commit containing this manifest is the R1 `candidate_sha`. The verifier must read the named files from that exact commit, confirm every listed SHA-256 value, and avoid the moving working tree. This manifest cannot list its own file hash without changing itself.

## Candidate Files and Pre-Commit Hashes

| File | SHA-256 |
|---|---|
| `source-index.md` | `281FDD8D2311EC9BD9E2A17964662A0E4B410FF04435FEE19CAAB9063E0FD363` |
| `exp-02-goal-and-measurement-contract-v0.1.md` | `E076CEE72CB4D968BE008C277D9CD513464D4DC2A81FEDC1B40592D475DFC6D6` |
| `exp-02-researcher-return-v0.1.md` | `76373967A116E19C1E9740AD561EA26EC14F7E5B41FF5280BCE3340DE14B9078` |
| `exp-02-researcher-return-qualification-v0.1.md` | `CBE7E9B706B69E3726B0255447304591C8AB8C75693BFEE19A22780D3A2067B6` |
| `exp-02-post-meeting-execution-candidate-v0.1.md` | `5EA7A5E2376F59986C91E20E475E9F84DDEEEE7CD3E202274F54492889CE4240` |
| `exp-02-verifier-return-v0.1.md` | `ECA5C2100A5C8CDE235A8D1D4CA4E33AFA90AB97E592757B3FF124187DFF585D` |
| `human-decision-record-exp-02-r1-authorization-v0.1.md` | `B73B93119D20C24B08C70DDFE3CDD32CBC1DF3A4DF8595081773CC0BAD04691B` |
| `exp-02-r1-executor-contract-v0.1.md` | `523E552E2DC942B675482B5358C3DE1505248A609C5AC1CE6694339442D106A4` |
| `exp-02-r1-lane-ledger-v0.1.md` | `19CE69F4927EFF7BD3324D6CC5B9B539FAF79E58A3C285A23A3965AC1FDA910A` |
| `exp-02-r1-post-meeting-execution-candidate-v0.1.md` | `E50AF0946D27231CBF9D3BD7BF2A14E8C51D03401C4156E70395F0AD767A30AF` |
| `exp-02-r1-executor-return-v0.1.md` | `B3EF9D2EFC3B86FB8317200D659CB528BE72E7833A9523EECEE464DC6E4630BF` |
| `exp-02-r1-root-reconciliation-v0.1.md` | `87BDE859CEEEBB2C440CBBBB3B420F64BD9D21569CF045D1F7EB96472BD94D5F` |
| `exp-02-r1-verifier-intake-v0.1.md` | `6948182F16ABB8B26C47095CE1BAE7D9DACE46C74386A3A931B65CE9C78DD47F` |

All paths are relative to `runs/2026-07-15/`.

## Recovery Path Versus Manifest Scope

The manifest contains `13` files for integrity checking. The candidate's recovery-burden test uses exactly five physical files. These are separate concepts: manifest scope protects the full review set; recovery scope measures the smallest bounded path to goal, lineage, candidate, and evidence.

## Excluded Worktree State

Existing changes to `AGENTS.md` and `runs/2026-07-14/` are user work outside this R1 candidate. They must not be staged or committed. Original EXP-02 files are listed as unchanged dependencies; they are not modified by R1.

## Proof Boundary

The candidate commit freezes review evidence only. It does not create acceptance, validation, runtime readiness, automation, skill/eval or permanent-agent promotion, frontend approval, infrastructure approval, canon, PR approval, `main` promotion, external posting, repo replacement, or a pass for the original EXP-02 candidate.
