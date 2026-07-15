---
title: EXP-02 Candidate Manifest
asset_type: candidate_manifest
status: ready_for_commit_freeze
version: v0.1
owner: Root Orchestrator
created: 2026-07-15
goal_id: EXP-02-PM2E-2026-07-15
candidate_sha: commit_containing_this_manifest
---

# EXP-02 Candidate Manifest

## Freeze Rule

The candidate is the exact set of files below as committed together on the current scoped branch. The resulting Git commit is the `candidate_sha`. This manifest does not contain its own SHA-256 because changing the manifest to add that hash would change the hash. The Git commit freezes the manifest itself.

## Candidate Files and Pre-Commit Hashes

| File | SHA-256 |
|---|---|
| `exp-02-executor-contract-v0.1.md` | `F15C7B4C640B88A33CD3A02A334CC0CB5BBBCB0E198154B3B62E1E6A25F4F8C5` |
| `exp-02-executor-return-v0.1.md` | `3807D414C6C85BF854C443CD081DC12EC63DF18B4A35300B87FC441232D78BE2` |
| `exp-02-goal-and-measurement-contract-v0.1.md` | `E076CEE72CB4D968BE008C277D9CD513464D4DC2A81FEDC1B40592D475DFC6D6` |
| `exp-02-lane-ledger-v0.1.md` | `B3DF128482BC847D0F7B3A624524885EBAEB3A6A1F185344CB9D8205B419ECF2` |
| `exp-02-post-meeting-execution-candidate-v0.1.md` | `5EA7A5E2376F59986C91E20E475E9F84DDEEEE7CD3E202274F54492889CE4240` |
| `exp-02-researcher-contract-v0.1.md` | `A94288D42FB65F2FCE95DD4056B61F3E5864A827D4FA1046DF4E2CC6201EB218` |
| `exp-02-researcher-return-qualification-v0.1.md` | `CBE7E9B706B69E3726B0255447304591C8AB8C75693BFEE19A22780D3A2067B6` |
| `exp-02-researcher-return-v0.1.md` | `76373967A116E19C1E9740AD561EA26EC14F7E5B41FF5280BCE3340DE14B9078` |
| `exp-02-root-reconciliation-v0.1.md` | `6A0D1CC3D98FDBE34B3AEA9C4995AD01A38CCFF105F6167BBB66A9F39E4ECE13` |
| `exp-02-verifier-intake-v0.1.md` | `B56ACE94B660C083A7BF53A3B451446F8F09684C56EF6DA3B694ED4B4D51593B` |
| `human-decision-record-exp-02-authorization-v0.1.md` | `301494D67201CA8F58AE03229206E4C30C13F8B4195AA3D42FA4C8F7763AA457` |
| `source-index.md` | `32041DF3D75848B76FFDAD94F1EC6153AEC36006FD5ECA38F7B234A5F9D26C4E` |

All paths are relative to `runs/2026-07-15/`.

## Excluded Worktree State

Existing modifications outside `runs/2026-07-15/`, including `AGENTS.md` and local July 14 experiment files, are not part of this candidate and must not be staged or committed with it.

## Verification Intake

The root must give the independent verifier:

- the exact candidate commit SHA;
- this manifest at that SHA;
- the frozen goal and measurement contract;
- the candidate and specialist returns;
- the root reconciliation;
- confirmation that no candidate file will move during review.

Commit and verification do not create human acceptance, validation, runtime readiness, infrastructure approval, canon, automation, skill promotion, or repo replacement.
