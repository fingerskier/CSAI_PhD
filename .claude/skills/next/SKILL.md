---
name: next
description: Quick orientation — where am I in the program and what should I do right now? Use for "/next", "what should I work on?", "where was I?", or when a new learner doesn't know where to start. For full planning meetings use /advisor instead.
---

# What's Next

A two-minute dispatch, not a meeting. Read the workspace state, tell the user where they are, and point them at exactly one next action with the skill that does it. If they want to plan the week or contest the priority, hand off to `/advisor`.

## Read state (fast)

1. `milestones/roadmap.md` + anything in `milestones/` — current phase and its exit criteria.
2. `research/error-log.md` (if present) — entries whose +48h re-attempt date has arrived.
3. Recent activity — `git log --oneline -15` and newest files under `research/` — what's actually in flight.
4. `assessments/` — has the diagnostic been completed?

## Dispatch rules (priority order)

1. **Fresh workspace** (empty `research/`, no filled diagnostic) → start with `assessments/diagnostic.md`, Phase 0. Briefly introduce the toolkit table from `CLAUDE.md` so they know what exists.
2. **Overdue re-attempts** → these come first; reinforcement compounds. Route to `/quiz` (or `/flashcards` review) on the overdue items.
3. **In-flight artifact** (half-done replication, draft proposal, module mid-pass) → resume it; name the file and the skill that owns it. Don't suggest starting anything new while something decisive is half-done.
4. **Module cadence** — if the current module's recent quiz scores are at threshold (≥85% × 3 spaced), suggest `/oral-exam` for the defense pass; otherwise the next `/study` or `/quiz` iteration.
5. **Nothing in flight, no module open** → recommend the next core module per `curriculum/core/README.md` ordering and the user's phase, starting with `/study`.

## Output format

Keep it to roughly:

- **You are:** phase, current module/project, one-line evidence (last artifact + date).
- **Due:** overdue error-log re-attempts, if any.
- **Next action:** one concrete step with its skill invocation (e.g. "`/quiz distributed-systems` — re-attempt the two linearizability misses from June 5").
- **Also available:** only if the user seems unaware of a relevant skill; otherwise skip.

One recommendation, not a menu. If the user pushes back, that's a conversation for `/advisor`.
