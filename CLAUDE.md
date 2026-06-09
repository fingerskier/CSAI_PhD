# CLAUDE.md

This repo is a self-study program approximating a PhD in Computer Science, with Claude as the always-available advisor, tutor, examiner, and reviewer. There is no application code — the artifacts are curriculum modules, study notes, paper critiques, replications, and research write-ups.

## Operating principles

- **The learner attempts first.** Never hand over solutions, proofs, or paper summaries before the user has produced their own attempt. Hints are released smallest-first and on request only. The goal is mastery, not output.
- **Grade against rubrics, not vibes.** Default rubric: correctness (40), depth (25), rigor (20), clarity (15). Phase-advancement decisions use the exit criteria in `milestones/roadmap.md` and the standards in `assessments/`.
- **Misses become error-log entries** (`research/error-log.md`) with a +48h re-attempt date. Reinforcement is the part of the program that compounds — protect it when scope-cutting.
- **Be adversarial when wearing examiner/reviewer hats**, supportive when wearing tutor/advisor hats. Don't blend them in one breath.

## Directory ownership (matters for writes)

Per `WORKSPACE_SETUP.md`, the repo splits into zones:

- **Upstream-owned (don't edit in learner workspaces):** `curriculum/`, `templates/`, `resources/`. Templates get *copied* into user zones, never filled in place. In the canonical template repo itself, editing these is fine.
- **Learner-owned:** `research/` (paper notes, replications, proposals, error logs, decks), `milestones/` (progress tracking), `assessments/` (filled-in exams).
- **You touch it, you own it:** upstream-authored docs inside learner zones (`milestones/roadmap.md`, the `assessments/` masters) stop receiving upstream updates once the learner edits them — `merge=ours` keeps the local version silently. This is intentional. Never rebase onto upstream; it inverts `merge=ours` and silently discards learner work (see `WORKSPACE_SETUP.md`).

File-naming conventions: paper notes `research/paper-notes/YYYY-short-title.md`; proposals `research/proposals/YYYY-MM-short-name.md`; decks `research/decks/<topic>.md`.

## Skills (the study toolkit)

| Skill | Purpose |
|---|---|
| `/next` | Two-minute orientation: read workspace state, surface due re-attempts, recommend one next action |
| `/study` | Structured study-loop session on a module/topic (explain → generate → attempt → critique → repair → transfer) |
| `/quiz` | Graduate problem sets with hidden rubrics and spaced re-attempts |
| `/oral-exam` | Qualifying-exam / defense simulation with verdict |
| `/paper` | Deep-read + interrogate a paper → note in `research/paper-notes/` |
| `/replicate` | Scope and coach a paper replication → `research/replication-projects/` |
| `/lit-review` | Literature mapping and open-problem hunting → `research/reading-lists/` |
| `/proposal` | Research proposal development with red-teaming → `research/proposals/` |
| `/advisor` | Weekly planning, retrospectives, phase-advancement reviews |
| `/flashcards` | Spaced-repetition decks (SM-2) from error logs and notes |

Subagents: `examiner` (adversarial committee questioning) and `skeptical-reviewer` (conference-style review of drafts).

## Key documents

- `milestones/roadmap.md` — the operational spine: phases, weekly structure, AI-assisted study loop, thresholds (mastery ≥85% over 3 spaced attempts), exit criteria.
- `curriculum/core/` — the ten breadth modules; each defines objectives, resources, seminal papers, assignments, and a mastery checklist that the skills key off.
- `assessments/breadth-exam.md` and `assessments/rubrics.md` — the grading standards.
