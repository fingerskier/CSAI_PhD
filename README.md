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

1. Create your own workspace from this template — see [`WORKSPACE_SETUP.md`](WORKSPACE_SETUP.md).
2. Start with [`milestones/roadmap.md`](milestones/roadmap.md).
3. Complete the diagnostic in [`assessments/diagnostic.md`](assessments/diagnostic.md).
4. Work through core modules in [`curriculum/core/`](curriculum/core/).
5. Maintain paper notes using [`templates/paper-note.md`](templates/paper-note.md).
6. Complete replication and original research projects under [`research/`](research/).
7. Use milestone reviews to decide when to advance phases.

## Updating your workspace from upstream

Your workspace is a copy of this template, with this repo tracked as the `upstream` remote so curriculum updates can flow in. One-time setup (full details in [`WORKSPACE_SETUP.md`](WORKSPACE_SETUP.md)):

```bash
git remote add upstream https://github.com/fingerskier/CSAI_PhD.git
git config --global merge.ours.driver true   # activate the merge=ours rules in .gitattributes
git config --global pull.rebase false        # see the warning below
```

When upstream publishes new modules, templates, or resources, pull them in with a merge:

```bash
git fetch upstream
git merge upstream/main
```

The `merge=ours` rules in `.gitattributes` keep your filled-in work in `research/`, `milestones/`, and `assessments/` from being clobbered if upstream touches the same paths.

> **Merge, never rebase.** Don't `git rebase upstream/main` and don't `git pull --rebase` from upstream. A rebase swaps the meaning of "ours", so the `merge=ours` rules keep *upstream's* side and silently discard your commits on protected paths — the rebase reports success, and your work is gone from history.

To sync only the upstream-owned zones without merging anything else:

```bash
git fetch upstream
git checkout upstream/main -- curriculum/ templates/ resources/
git commit -m "Sync curriculum from upstream"
```

Two caveats, both by design:

- Upstream-authored files inside your zones (`milestones/roadmap.md`, the `assessments/` masters) stop receiving upstream updates the first time you edit them — `merge=ours` keeps your version silently. See ["You touch it, you own it"](WORKSPACE_SETUP.md#you-touch-it-you-own-it) for how to view or take upstream's version manually.
- If a merge surfaces a real conflict, resolve it by hand (`git status`, edit, `git add <file>`, `git merge --continue`); `git merge --abort` backs out.

## Important note

This is not an accredited PhD program and does not grant a degree. It is a structured self-study and research training program modeled on PhD-level expectations.
