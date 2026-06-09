---
name: quiz
description: Generate and grade a graduate-level problem set on a topic or module, with hidden rubric and spaced-repetition follow-up. Use for "/quiz algorithms", "test me on consensus protocols", or timed mock-exam practice.
---

# Quiz / Problem Set

Generate a graduate-level problem set on the topic in the arguments and grade the user's attempts. If no topic is given, ask — or offer a mixed-domain set drawn from the sections in `assessments/breadth-exam.md`.

## Generating

- Default set: 5 problems — 2 conceptual, 2 quantitative/proof, 1 open-ended design or research-style question. Honor explicit requests for different sizes or formats.
- Pull difficulty from the relevant module in `curriculum/core/`: problems should require the module's mastery-checklist skills, not recall.
- Write a rubric per problem **before** presenting the set, but keep it hidden until grading.
- If the user asks for a **timed** set, state the time budget per problem up front (use breadth-exam pacing: ~20–30 min per problem).
- If an error log exists in `research/`, include at least one variant of a previously missed problem that is due for re-attempt.

## Grading

- Wait for the user's attempt. Release hints only on request, smallest first; each hint caps the problem score (note the cap when giving the hint).
- Grade each problem: correctness (40), depth (25), rigor (20), clarity (15). Show the rubric now, quote the specific gap, and state the minimum change for full marks.
- Distinguish *slips* (knew it, botched execution) from *gaps* (missing concept). Gaps get logged; slips get a quick re-drill.

## After grading

- Report the set score against the program's mastery threshold (≥85% across 3 spaced attempts, per `milestones/roadmap.md`).
- Append misses to the error log under `research/` with a +48h re-attempt date.
- If the user has passed three spaced sets on this topic at ≥85%, say so explicitly — that's the signal to advance per the roadmap exit criteria.
