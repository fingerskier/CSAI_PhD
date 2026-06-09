# CSAI_PhD

A self-study program designed to approximate the breadth, rigor, and research expectations of a PhD-level Computer Science education for a participant with a B.S. in CS or a related field and professional software/engineering experience.

> Focus: Computer Science foundations, AI/ML, systems, theory, research methods, and optional control-systems + AI integration.

## Program goals

By the end of the program, the participant should be able to:

- Master graduate-level CS foundations across algorithms, systems, theory, AI/ML, and research methodology.
- Read, critique, reproduce, and extend peer-reviewed research.
- Build a research portfolio with paper summaries, replication studies, original prototypes, and a dissertation-style capstone.
- Demonstrate PhD-like independence: formulating problems, surveying literature, designing experiments, and communicating results.

## Assumptions

This program assumes the learner already has:

- B.S.-level programming, data structures, algorithms, discrete math, operating systems, and probability/statistics exposure.
- Professional experience building non-trivial software or technical systems.
- Ability to study independently for 10–20 hours/week over multiple years.

## Repository structure

```text
.
├── .claude/                # Claude Code skills and agents for AI-augmented study
├── curriculum/             # Core, advanced, and specialization study modules
├── research/               # Reading lists, paper notes, replications, proposals
├── milestones/             # Year-by-year qualification and research milestones
├── assessments/            # Exams, rubrics, project evaluation checklists
├── templates/              # Reusable templates for notes, reviews, proposals
├── resources/              # Books, courses, tools, datasets, conferences
└── scripts/                # Optional helper scripts
```

## AI-augmented study toolkit

The repo ships with [Claude Code](https://code.claude.com/docs) skills that implement the AI-assisted workflow from the [roadmap](milestones/roadmap.md). Open the repo in Claude Code and invoke them as slash commands:

| Skill | What it does |
|---|---|
| `/next` | Quick orientation: where you are in the program and the one thing to do next |
| `/study <module>` | Guided study loop: explain → generate → attempt → critique → repair → transfer |
| `/quiz <topic>` | Graduate-level problem sets with hidden rubrics and spaced re-attempts |
| `/oral-exam <topic>` | Qualifying-exam simulation with adversarial probing and a verdict |
| `/paper <title/link>` | Deep-read and interrogate a paper → structured note in `research/paper-notes/` |
| `/replicate <paper>` | Scope and coach a replication project end to end |
| `/lit-review <area>` | Literature mapping, clustered reading queues, open-problem hunting |
| `/proposal <idea>` | Research proposal development with Heilmeier framing and red-teaming |
| `/advisor` | Weekly planning, retrospectives, and phase-advancement reviews |
| `/flashcards <topic>` | Spaced-repetition decks (SM-2) built from your error log and notes |

Two subagents back the adversarial workflows: `examiner` (committee-style oral questioning) and `skeptical-reviewer` (conference-style review of your drafts). Conventions for all of this live in [`CLAUDE.md`](CLAUDE.md).

## Suggested timeline

| Phase | Duration | Emphasis |
|---|---:|---|
| Phase 0 | 1–2 months | Diagnostic review and math/programming refresh |
| Phase 1 | 9–12 months | Graduate CS core breadth |
| Phase 2 | 9–12 months | Advanced topics and research literacy |
| Phase 3 | 12–18 months | Specialization, paper replications, original projects |
| Phase 4 | 12–24 months | Dissertation-style research agenda and capstone |

## How to use this repo

1. Start with [`milestones/roadmap.md`](milestones/roadmap.md).
2. Complete the diagnostic in [`assessments/diagnostic.md`](assessments/diagnostic.md).
3. Work through core modules in [`curriculum/core/`](curriculum/core/).
4. Maintain paper notes using [`templates/paper-note.md`](templates/paper-note.md).
5. Complete replication and original research projects under [`research/`](research/).
6. Use milestone reviews to decide when to advance phases.

## Important note

This is not an accredited PhD program and does not grant a degree. It is a structured self-study and research training program modeled on PhD-level expectations.
