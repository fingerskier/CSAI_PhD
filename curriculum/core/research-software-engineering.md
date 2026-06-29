# Research Software Engineering and Reproducibility

The engineering discipline that makes research artifacts credible: versioned code, tests, environments, experiment tracking, data provenance, packaging, documentation, and reproducible execution. This module closes the gap between prototype and inspectable scientific evidence.

## Learning objectives

- Build research code that another person can install, run, test, and modify.
- Capture environments and dependencies with containers, lockfiles, or reproducible package managers.
- Design experiment pipelines with configuration management, deterministic seeds where possible, logging, metadata, and artifact versioning.
- Write tests for scientific code: unit, property, regression, numerical-tolerance, data-validation, and end-to-end smoke tests.
- Maintain data provenance: raw/processed splits, checksums, licenses, schemas, and privacy constraints.
- Package results with scripts that regenerate key figures/tables from raw or documented intermediate artifacts.

## Prerequisites

- Professional programming experience and version-control fluency.
- [Research Methods](research-methods.md) for reproducibility expectations.
- [Statistics and Experimental Design](statistics-experimental-design.md) for evidence and analysis standards.

## Primary resources

- **Wilson et al., "Good Enough Practices in Scientific Computing"** — pragmatic baseline for research workflows.
- **The Turing Way** — reproducible, collaborative, and ethical research practices.
- **Software Carpentry lessons** — command line, Git, testing, automation, and packaging refreshers.
- **Kitzes, Turek & Deniz, *The Practice of Reproducible Research*** — case studies and workflow patterns.
- **Pineau et al., "Improving Reproducibility in Machine Learning Research"** — ML-specific checklist and reporting norms.

## Seminal papers and reports

- Buckheit & Donoho (1995), "WaveLab and Reproducible Research."
- Claerbout & Karrenbach (1992), "Electronic Documents Give Reproducible Research a New Meaning."
- Sandve et al. (2013), "Ten Simple Rules for Reproducible Computational Research."
- Wilson et al. (2014), "Best Practices for Scientific Computing."
- Stodden, Leisch & Peng (2014), *Implementing Reproducible Research*.
- Tatman, VanderPlas & Dane (2018), "A Practical Taxonomy of Reproducibility for Machine Learning Research."
- Pineau et al. (2021), "Improving Reproducibility in Machine Learning Research."

## Assignments

- **Reproducibility harness:** take an existing project in this repo and add a one-command smoke test, environment file, README instructions, and expected output checksum or metric range.
- **Experiment tracker:** run a small experiment with configuration files, immutable run IDs, logs, plots, and a manifest mapping figures/tables to commands.
- **Data provenance audit:** document a dataset's source, license, schema, preprocessing, splits, checksums, privacy constraints, and known biases.
- **Testing lab:** add unit/property/regression tests to a research prototype, including one test that would have caught a real bug or result discrepancy.
- **Artifact review:** review someone else's artifact or an open-source replication package and file a structured reproducibility report.

## AI study loop

- `/study research-software-engineering` for workflow design; ask for minimal robust tooling before adopting heavy infrastructure.
- `/replicate <paper>` with the instruction: produce an artifact manifest, environment plan, and clean-room runbook before implementation.
- `/proposal <idea>` with explicit reproducibility deliverables: tests, data versioning, experiment tracking, and figure regeneration.
- `/oral-exam research-software-engineering` — expect "could I rerun this in six months?" and "what breaks if a dependency changes?"

## Mastery checklist

- [ ] Can package a research artifact so a fresh environment can run the main result from documented commands.
- [ ] Can write tests that protect core scientific claims, not only code paths.
- [ ] Can trace every reported figure/table to data, code, configuration, and environment metadata.
- [ ] Can explain nondeterminism sources and bound or report their effect.
- [ ] Can document dataset provenance, licensing, privacy constraints, and preprocessing.
- [ ] Can perform a structured artifact review and identify reproducibility blockers.

## Where next

Apply this module to every implementation project, replication, and capstone. It is particularly important for [Databases](databases.md), [Distributed Systems](distributed-systems.md), [Machine Learning Foundations](machine-learning.md), [Deep Learning Systems](../advanced/deep-learning-systems.md), [High-Performance Computing](../advanced/high-performance-computing.md), and [Scientific Computing](../advanced/scientific-computing.md).
