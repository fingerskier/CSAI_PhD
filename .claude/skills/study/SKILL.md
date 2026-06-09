---
name: study
description: Run a structured AI-assisted study session on a curriculum module or topic. Use when the user wants to learn, review, or work through material — e.g. "/study distributed-systems", "study Paxos with me", or "let's work on the ML module".
---

# Study Session

Run one iteration of the repo's study loop (defined in `milestones/roadmap.md`) on the topic given in the arguments. If no topic is given, ask which module or concept to work on, listing the modules in `curriculum/core/`.

## Setup

1. If the topic maps to a module, read its file in `curriculum/core/` (or `curriculum/specializations/`) and anchor the session to its learning objectives and mastery checklist.
2. Check `research/` for the user's existing notes or error logs on this topic and calibrate difficulty accordingly. Don't re-teach what their notes show they've mastered; target weaknesses.

## The loop

Work through these stages, one at a time, conversationally:

1. **Explain** — teach the concept in three passes: intuition, formalism, implementation. Name the standard misconceptions and edge cases explicitly. Cite where this sits in the module's primary resources so the user can deep-read later.
2. **Generate** — produce 3–5 exercises at increasing difficulty: at least one conceptual, one quantitative/proof, one open-ended. Keep your rubric hidden.
3. **Attempt first** — the user solves before you reveal anything. Give hints only when asked, smallest hint first. Never volunteer the answer.
4. **Critique** — grade their solution against the hidden rubric: correctness (40), depth (25), rigor (20), clarity (15). State the minimum changes needed for full marks.
5. **Repair** — for anything below full marks, append an entry to the user's error log (suggest `research/error-log.md` if none exists): topic, mistake, root cause, scheduled re-attempt date (+48h).
6. **Transfer** — pose one question applying the same concept in a different domain (e.g. a queueing concept applied to GPU scheduling).

## Session close

- Summarize: what was covered, scores, gaps logged, what to re-attempt and when.
- Update nothing in `curriculum/` — that zone is upstream-owned. All user artifacts go under `research/`.
- Suggest the natural next step: another loop iteration, `/quiz` for volume practice, or `/oral-exam` if the mastery checklist looks close to complete.
