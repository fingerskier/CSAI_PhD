# Statistics and Experimental Design for CS Research

The empirical backbone of computer science research: statistical inference, causal thinking, benchmark design, measurement validity, and uncertainty reporting. This module turns "the experiment ran" into evidence that can survive reviewer scrutiny.

## Learning objectives

- Design experiments with explicit hypotheses, variables, controls, power considerations, and pre-specified analysis plans.
- Use probability and statistical inference correctly: confidence/credible intervals, bootstrap, hypothesis tests, effect sizes, multiple-comparison correction, and Bayesian updating.
- Distinguish prediction, association, and causation; use randomized experiments, natural experiments, difference-in-differences, instrumental variables, and causal graphs at the level needed to critique CS papers.
- Evaluate benchmarks: dataset construction, train/test leakage, distribution shift, workload representativeness, confounders, baselines, ablations, and external validity.
- Analyze performance and systems measurements with appropriate replication, blocking, variance decomposition, and nonparametric summaries.
- Communicate uncertainty honestly through tables, plots, error bars, negative results, and limitations.

## Prerequisites

- [Mathematics for CS Research](math-for-cs.md) — probability, statistics, and linear algebra.
- [Research Methods](research-methods.md) — paper critique and reproducibility workflow.
- Programming fluency in Python or R for analysis notebooks.

## Primary resources

- **Wasserman, *All of Statistics*** — compact mathematical statistics reference.
- **Gelman, Hill & Vehtari, *Regression and Other Stories*** — modeling workflow, uncertainty, and diagnostics.
- **Cunningham, *Causal Inference: The Mixtape*** — causal designs with practical examples.
- **Jain, *The Art of Computer Systems Performance Analysis*** — still the standard for systems measurement methodology.
- **Kohavi, Tang & Xu, *Trustworthy Online Controlled Experiments*** — A/B testing, guardrails, and experimentation pitfalls.
- **Goodfellow, Bengio & Courville, *Deep Learning*, evaluation sections** plus modern benchmark papers for ML-specific evaluation failure modes.

## Seminal papers

- Fisher (1935), *The Design of Experiments* — randomization and experimental logic.
- Neyman (1923/1990 translation), "On the Application of Probability Theory to Agricultural Experiments" — potential outcomes.
- Efron (1979), "Bootstrap Methods: Another Look at the Jackknife."
- Pearl (1995), "Causal Diagrams for Empirical Research."
- Demšar (2006), "Statistical Comparisons of Classifiers over Multiple Data Sets."
- Drummond (2009), "Replicability is Not Reproducibility: Nor is it Good Science."
- Henderson et al. (2018), "Deep Reinforcement Learning that Matters."
- Sculley et al. (2018), "Winner's Curse? On Pace, Progress, and Empirical Rigor."
- Recht et al. (2019), "Do ImageNet Classifiers Generalize to ImageNet?"
- van der Kouwe et al. (2018), "Benchmarking Crimes: An Emerging Threat in Systems Security."

## Assignments

- **Problem sets:** weekly exercises on estimators, intervals, bootstrap, test selection, causal graphs, power, and multiple comparisons.
- **Benchmark audit:** choose one ML, systems, or HCI paper and reconstruct its claim-evidence chain. Identify variables, controls, baselines, uncertainty, threats to validity, and one missing robustness check.
- **Reanalysis project:** reproduce the statistical analysis from a published paper or open benchmark. Recompute intervals/effect sizes, test sensitivity to outliers and seeds, and write a corrected results section.
- **Experimental design proposal:** before running any new experiment, submit a pre-analysis plan with hypothesis, units of analysis, stopping rule, sample-size rationale, metrics, exclusion criteria, and planned plots.
- **Measurement lab:** run a small performance experiment with blocking/randomization, at least 30 repeated measurements where appropriate, and a variance analysis explaining noise sources.

## AI study loop

- `/study statistics-experimental-design` for concept passes; require the AI to ask for the claim and unit of analysis before suggesting a test.
- `/quiz statistics-experimental-design` weekly — emphasize choosing the right design, not just calculating p-values.
- `/paper <empirical paper>` with an added instruction: produce a threat-to-validity table and a minimum additional experiment that could falsify the main claim.
- `/oral-exam statistics-experimental-design` — expect adversarial questions about confounding, leakage, multiple testing, and whether the evidence supports the claim.

## Mastery checklist

- [ ] Can translate a research claim into testable hypotheses, variables, controls, and success/failure criteria.
- [ ] Can choose and justify intervals/tests/effect sizes for common CS experiments, including non-normal performance data.
- [ ] Can identify leakage, confounding, benchmark overfitting, and external-validity failures in an empirical paper.
- [ ] Can construct and interpret a causal graph for a simple research design.
- [ ] Can produce plots/tables that communicate uncertainty without overstating conclusions.
- [ ] Can write a limitations section that distinguishes evidence, speculation, and future work.

## Where next

Use this module alongside every empirical advanced module. It is especially important before [Machine Learning Foundations](machine-learning.md), [Distributed Systems](distributed-systems.md), [Databases](databases.md), [Human-Computer Interaction](../advanced/human-computer-interaction.md), [Deep Learning Systems](../advanced/deep-learning-systems.md), and [Robotics and Control](../advanced/robotics-control.md).
