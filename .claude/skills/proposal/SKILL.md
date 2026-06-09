---
name: proposal
description: Develop a research proposal from idea to defensible document, including red-teaming the methodology. Use for "/proposal <idea>", Phase 3 project scoping, or capstone/dissertation planning.
---

# Research Proposal Development

Develop the research idea in the arguments into a proposal under `research/proposals/`, built from `templates/project-proposal.md`. This is the Phase 3/4 workflow from `milestones/roadmap.md`.

## Stage 1 — Problem framing

- Force the idea through the **Heilmeier catechism**: what are you trying to do (no jargon), how is it done today and what are the limits, what's new in your approach, who cares, what are the risks, what does it cost (time/compute), and how will you know you've succeeded?
- Establish the **literature delta** against `research/reading-lists/` and paper notes (run `/lit-review` first if the area is unmapped). The delta must name specific papers and state what they don't do — "nobody has tried X" requires evidence of looking.

## Stage 2 — Hypothesis and design

- State the central claim as a falsifiable hypothesis with numeric success **and failure** criteria committed in advance.
- Design the experiment/system plan including: baselines (the strongest ones, not the convenient ones), ablations that isolate each claimed contribution, and the robustness checks that could kill the hypothesis.
- Scope check: the first decisive result must be reachable in ≤12 weeks per the Phase 3 criteria. If not, slice the problem until it is.

## Stage 3 — Red team

Hand the draft to the `skeptical-reviewer` agent with instructions to attack: leakage paths, weak baselines, benchmark overfitting, p-hacking surface area, unfalsifiable claims, and scope realism. The user must revise or rebut every major point — unresolved attacks go in the proposal's own limitations section.

## Stage 4 — Commit

- File the proposal as `research/proposals/YYYY-MM-short-name.md` with a timeline of weekly milestones and named kill criteria ("abandon if X hasn't worked by week N").
- Schedule the first `/advisor` review of the project for 2 weeks out.
