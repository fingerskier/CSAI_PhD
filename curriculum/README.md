# Curriculum Guide and Gap Map

This curriculum is intentionally broad, but a PhD-style self-study plan needs explicit boundaries: what is required for breadth, what is optional depth, and where a learner must add material for a specific research direction. Use this guide before starting Phase 1 and revisit it at every milestone review.

## What is covered well

- **Graduate CS breadth:** algorithms, theory, math, ML, systems, databases, architecture, programming languages, and research methods are represented in the [core modules](core/README.md).
- **Research-facing depth:** advanced modules cover the most common continuations into AI/ML, systems, theory, control/robotics, HCI, scientific computing, and infrastructure.
- **Artifact-based evaluation:** most modules require proof work, implementation, measurement or replication, paper critique, oral defense, and a mastery checklist.
- **Cross-disciplinary paths:** specialization tracks connect core breadth to focused research portfolios.

## Known gaps and how to handle them

These areas are not first-class required modules. Treat them as gap-fillers when they are prerequisites for your research question.

| Gap area | Why it matters | Recommended treatment |
|---|---|---|
| **Statistics and experimental design beyond ML** | Many CS papers fail through weak causal claims, poor uncertainty estimates, or invalid benchmark comparisons. | Pair [Research Methods](core/research-methods.md) with probability/statistics units from [Mathematics for CS Research](core/math-for-cs.md); add a short module on causal inference, power analysis, multiple comparisons, and Bayesian data analysis if your work is empirical. |
| **Ethics, safety, privacy, and societal impact** | AI, security, HCI, data systems, and robotics all require explicit threat, harm, and governance analysis. | Include an ethics/threat-model section in every proposal and replication. AI/ML learners should add readings on dataset documentation, model evaluation harms, privacy, and alignment/safety. |
| **Software engineering for research** | PhD-level artifacts must be reproducible, maintainable, and reviewable, not just clever. | During every build pass, require tests, experiment scripts, environment capture, logging, and a short maintenance note. Systems/ML-systems learners may add a focused software-engineering module. |
| **Numerical/statistical computing foundations** | ML, graphics, robotics, simulation, and scientific ML often fail because of conditioning, floating point, or estimator issues. | Take [Scientific Computing](advanced/scientific-computing.md) if your work uses simulation, optimization, inverse problems, differentiable physics, or large numerical pipelines. |
| **Information theory and coding theory** | Useful in theory, ML, compression, distributed systems, communications, privacy, and learning theory. | Add as an elective reading thread under Theory or AI/ML when mutual information, entropy, compression, or channel models become central. |
| **Quantum computing, computational biology, graphics, economics/game theory** | Important CS subfields but outside the default scope. | Create a new advanced module using the template implied by existing modules: objectives, prerequisites, resources, seminal papers, assignments, AI loop, and checklist. |
| **Domain-specific research norms** | Publication standards differ by area: theory proofs, systems artifacts, ML benchmarks, HCI studies, robotics demos, etc. | For the chosen specialization, inspect recent top-venue papers and add venue-specific expectations to the proposal and capstone rubrics. |

## Ambiguities resolved

- **Core means required breadth.** Complete all core modules unless a diagnostic and advisor review explicitly waive a topic because the learner can already pass its mastery checklist.
- **Advanced means selected depth.** Do not complete every advanced module by default. Choose 2–4 modules tightly aligned with the primary specialization, plus at most 1–2 adjacent modules for breadth.
- **A module is not complete when the reading is complete.** Completion requires: passing spaced assessments, producing at least one durable artifact, defending the material orally, and recording unresolved weaknesses.
- **Paper counts are evidence, not goals.** A 50-paper list with shallow notes is weaker than 20 papers with claim-evidence maps, replications, and synthesis. Use counts as minimum exposure, not as a substitute for research judgment.
- **Implementation projects need evaluation.** A project without tests, baselines, ablations, measurement methodology, or a failure analysis does not satisfy the artifact bar.

## Recommended sequencing

1. **Phase 0:** run the diagnostic, repair math/probability/programming gaps, and choose tentative specialization interests.
2. **Phase 1 early:** take [Mathematics for CS Research](core/math-for-cs.md), [Algorithms and Complexity](core/algorithms-complexity.md), and [Research Methods](core/research-methods.md) early because they support the rest of the curriculum.
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
