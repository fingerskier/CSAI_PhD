# Curriculum Guide and Gap Map

This curriculum is intentionally broad, but a PhD-style self-study plan needs explicit boundaries: what is required for breadth, what is optional depth, and where a learner must add material for a specific research direction. Use this guide before starting Phase 1 and revisit it at every milestone review.

## What is covered well

- **Graduate CS breadth:** algorithms, theory, math, ML, systems, databases, architecture, programming languages, research methods, empirical design, responsible computing, and research software engineering are represented in the [core modules](core/README.md).
- **Research-facing depth:** advanced modules cover the most common continuations into AI/ML, systems, theory, control/robotics, HCI, scientific computing, and infrastructure.
- **Artifact-based evaluation:** most modules require proof work, implementation, measurement or replication, paper critique, oral defense, and a mastery checklist.
- **Cross-disciplinary paths:** specialization tracks connect core breadth to focused research portfolios.

## Gap-resolution modules

The first audit identified several areas that were too easy to treat as optional advice. They now have explicit curriculum homes:

| Former gap | Material update | How to use it |
|---|---|---|
| **Statistics and experimental design beyond ML** | [Statistics and Experimental Design for CS Research](core/statistics-experimental-design.md) | Required before serious empirical work; revisit for every benchmark, ablation, user study, systems measurement, or ML evaluation. |
| **Ethics, safety, privacy, and societal impact** | [Responsible Computing, Ethics, and Research Risk](core/responsible-computing.md) | Required for proposals, replications, datasets, model/system releases, and capstone go/no-go decisions. |
| **Software engineering for research** | [Research Software Engineering and Reproducibility](core/research-software-engineering.md) | Required for every implementation artifact; use its checklists before claiming a project is reproducible. |
| **Numerical/statistical computing foundations** | [Scientific Computing](advanced/scientific-computing.md), plus the new statistics module above | Take Scientific Computing when simulation, optimization, inverse problems, differentiable physics, or large numerical pipelines are central. |
| **Information theory and coding theory** | Elective thread within Theory or AI/ML | Still not required for all learners; add a focused advanced module if entropy, compression, channels, coding, or information-theoretic lower bounds become central. |
| **Quantum computing, computational biology, graphics, economics/game theory** | Custom advanced module | Create a new advanced module using the existing module structure when one of these becomes part of the research plan. |
| **Domain-specific research norms** | Specialization plan and venue audit | For the chosen specialization, inspect recent top-venue papers and add venue-specific expectations to the proposal and capstone rubrics. |

## Ambiguities resolved

- **Core means required breadth, including cross-cutting research practice.** Complete all core modules unless a diagnostic and advisor review explicitly waive a topic because the learner can already pass its mastery checklist.
- **Advanced means selected depth.** Do not complete every advanced module by default. Choose 2–4 modules tightly aligned with the primary specialization, plus at most 1–2 adjacent modules for breadth.
- **A module is not complete when the reading is complete.** Completion requires: passing spaced assessments, producing at least one durable artifact, defending the material orally, and recording unresolved weaknesses.
- **Paper counts are evidence, not goals.** A 50-paper list with shallow notes is weaker than 20 papers with claim-evidence maps, replications, and synthesis. Use counts as minimum exposure, not as a substitute for research judgment.
- **Implementation projects need evaluation.** A project without tests, baselines, ablations, measurement methodology, or a failure analysis does not satisfy the artifact bar.

## Recommended sequencing

1. **Phase 0:** run the diagnostic, repair math/probability/programming gaps, and choose tentative specialization interests.
2. **Phase 1 early:** take [Mathematics for CS Research](core/math-for-cs.md), [Algorithms and Complexity](core/algorithms-complexity.md), [Research Methods](core/research-methods.md), [Statistics and Experimental Design](core/statistics-experimental-design.md), and [Research Software Engineering](core/research-software-engineering.md) early because they support the rest of the curriculum.
3. **Phase 1 systems block:** take architecture → operating systems → distributed systems/databases, with programming languages either before or alongside systems if compilers or verification are likely interests.
4. **Phase 1 AI block:** take machine learning after math/probability foundations; revisit optimization and statistics as needed.
5. **Phase 2:** select advanced modules only after writing a one-page specialization plan with target venues, expected methods, and missing prerequisites.
6. **Phase 3+:** let the research question drive remaining study; add just-in-time mini-modules rather than expanding coursework indefinitely.

## Evidence standard for every module

A completed module should leave behind:

- a coverage map linking objectives to notes, problems, papers, and projects;
- at least three spaced assessment attempts with scores and corrections;
- one artifact another person can inspect or run;
- a paper critique or synthesis note connecting the module to active research;
- an oral-exam transcript or summary with unresolved questions;
- error-log entries for misses and a scheduled re-attempt.
