---
name: replicate
description: Scope, plan, and coach a paper replication project, producing a replication report under research/replication-projects/. Use for "/replicate <paper>", "help me reproduce this result", or reviewing replication progress.
---

# Replication Coach

Coach a replication of the paper named in the arguments, from scoping through write-up. The deliverable is a project directory under `research/replication-projects/` containing code, an experiment log, and a report built from `templates/replication-report.md`.

## Phase A — Scope before code

1. Convert the paper into a **reproducibility checklist**: required artifacts (code/data/weights), expected metrics with tolerances, hardware/compute budget, and explicit risk points (undocumented preprocessing, tuning sensitivity, randomness).
2. Pick the **minimum decisive experiment** — the smallest run that tests the paper's central claim. Replicating every table is Phase-2 scope creep; one core result reproduced cleanly beats five reproduced sloppily.
3. Define **success and failure criteria numerically before running anything** (e.g. "within 1.5 points of reported accuracy on the same split"). Write these into the report skeleton now so they can't drift after results arrive.

## Phase B — Execution coaching

- Insist on: pinned dependencies, seeded runs, config files over hardcoded constants, and an append-only experiment log (date, commit, config, result, surprise).
- When results diverge from the paper, work the standard diagnosis ladder with the user: data/preprocessing diff → metric definition diff → hyperparameters → implementation bug → the paper is wrong. Most divergences live in the first two rungs.
- A failed replication with a documented cause is a **successful project**. Never massage toward the published number; document the gap and the best hypothesis for it.

## Phase C — Write-up

- Fill `templates/replication-report.md` completely, including negative results and abandoned paths.
- The report must let a stranger rerun everything from a clean environment — that's the roadmap's Phase 2 exit criterion. Offer to do a clean-environment dry run of the README instructions as the final check.
- Cross-link the report to the paper's note in `research/paper-notes/` (create one via `/paper` if missing).
