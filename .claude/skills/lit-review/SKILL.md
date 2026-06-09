---
name: lit-review
description: Build or extend a literature survey on a research area — search, triage, map the field, and identify open problems. Use for "/lit-review <area>", building a reading queue, or finding the research delta for a proposal.
---

# Literature Review

Build a literature map for the area in the arguments, producing a survey document under `research/reading-lists/` (queue + map) and, when requested, a full written survey under `research/`.

## Building the map

1. **Seed** — start from papers the user already has in `research/paper-notes/`, the seminal-papers lists in the relevant `curriculum/` module, and (if web access is available) recent surveys and the citation graph around them.
2. **Triage** — for each candidate paper record one line: claim, method family, venue/year, and why it's in or out. Target a queue of 20–50 papers organized into 3–6 thematic clusters, not a flat list.
3. **Map structure** — for each cluster identify: the founding paper, the current state of the art, the standing disagreement (every live field has one), and what evidence would settle it.
4. **Delta hunting** — the survey's job is to end in open problems. For each cluster, state: what's underexplored, why (hard? unfashionable? recently unblocked?), and a feasible 12-week problem slice per the Phase 3 criteria in `milestones/roadmap.md`.

## Quality bar

- Every claim about a paper must be checkable — cite the specific paper, never "studies show".
- Coverage honesty: explicitly list what the survey does *not* cover and why the boundary is drawn there.
- Recency check: if the newest paper in a cluster is >2 years old, either justify the cluster as settled or flag the search as incomplete.

## Outputs

- `research/reading-lists/<area>.md` — clustered, annotated queue with priorities.
- Each deep-read paper gets its own note via the `/paper` workflow.
- Full survey (when requested): problem framing → cluster-by-cluster synthesis → comparison table → open problems ranked by value/feasibility. Have the `skeptical-reviewer` agent attack the draft before calling it done.
