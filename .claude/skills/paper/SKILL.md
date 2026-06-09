---
name: paper
description: Deep-read and interrogate a research paper, producing a structured paper note in research/paper-notes/. Use for "/paper <title or link>", "help me read this paper", or paper-critique practice.
---

# Paper Digestion

Guide a deep read of the paper named in the arguments (title, arXiv link, or PDF path). Output: a completed note in `research/paper-notes/`, built from `templates/paper-note.md`.

## Process

1. **Acquire** — if given a link and web access is available, fetch the abstract and key sections. If given a local file, read it. Otherwise work from the user's description and ask them to paste key passages.
2. **Triage first (10–15 min discipline)** — before deep reading, have the user state from title/abstract/figures alone: the claimed contribution, the likely method, and what evidence would convince them. Deep reading then confirms or falsifies these guesses — this trains research taste.
3. **Interrogate, don't summarize.** Walk the paper through the roadmap's interrogation frame:
   - Assumptions — what must be true for this to work? Which are unstated?
   - Novelty — what is the actual delta over prior work? Quote the prior work.
   - Baselines — are they strong, current, and fairly tuned?
   - Threats to validity — confounds, leakage, benchmark overfitting, cherry-picked metrics.
   - Reproducibility gaps — what's missing to rerun this? Code, data, hyperparameters, compute?
   - Strongest follow-up — the single best next experiment, and the experiment that would *falsify* the paper.
4. **Socratic mode by default** — ask the user for their read on each dimension before giving yours. Disagree where warranted; the goal is calibrated judgment, not consensus.
5. **Write the note** — fill every section of the template. File it as `research/paper-notes/YYYY-short-title.md`. The "Questions" and "Follow-up ideas" sections must be non-empty — a note without open questions means the read was too shallow.

## Optional second pass

On request, hand the paper to the `skeptical-reviewer` agent for a conference-style review (5 major + 5 minor comments) and have the user rebut it as if they were the authors. This is the Phase 2 reviewer-calibration exercise from the roadmap.

## Connections

Always end by checking `research/paper-notes/` for related notes and adding cross-links to the "Connections to other work" section in both directions.
