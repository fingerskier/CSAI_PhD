# Research Methods

The craft of research itself: reading critically, designing experiments that can fail, writing and reviewing, managing a research program, and reproducibility — the module that turns the other nine into a PhD-shaped capability rather than coursework.

## Learning objectives

- Read papers in structured passes (triage → deep read → reproduce-or-derive → extend) and produce critiques that identify real threats to validity, not surface complaints.
- Design experiments scientifically: falsifiable hypotheses, success/failure criteria fixed in advance, strong baselines, ablations, and statistical reporting (seeds, variance, significance, effect sizes).
- Recognize and avoid the standard pathologies: data leakage, benchmark overfitting, p-hacking, HARKing, weak baselines, and survivorship in literature reviews.
- Write research prose: claim-evidence structure, the related-work section as argument rather than catalog, and figures that carry the paper.
- Review and be reviewed: produce a useful conference-style review; respond to one with rebuttals rather than capitulation or defensiveness.
- Run a research program: problem selection (taste), scoping to decisive 12-week slices, experiment logging, and knowing when to kill a project.
- Build a fully reproducible research package: pinned environments, seeded runs, one-command figure regeneration.

## Prerequisites

- Statistics from [Mathematics for CS Research](math-for-cs.md). Start this module early and run it *concurrently* with everything else — it is practiced, not completed.

## Primary resources

- **Keshav, "How to Read a Paper"** — the three-pass method; adopt it immediately.
- **Zobel, *Writing for Computer Science*** — the writing spine.
- **Booth et al., *The Craft of Research*** — argument structure (claims, reasons, evidence, warrants).
- **Hamming, "You and Your Research"** (1986 talk) — problem selection and research courage.
- **The Heilmeier Catechism** — the proposal-framing checklist (built into `/proposal`).
- **Pineau et al., "Improving Reproducibility in Machine Learning Research"** + the NeurIPS reproducibility checklist.
- **The Turing Way** (online handbook) — reproducible computational research practices.

## Seminal papers

- Hamming (1986), "You and Your Research".
- Keshav (2007), "How to Read a Paper".
- Ioannidis (2005), "Why Most Published Research Findings Are False".
- Demšar (2006), "Statistical Comparisons of Classifiers over Multiple Data Sets".
- Sculley et al. (2018), "Winner's Curse? On Pace, Progress, and Empirical Rigor".
- Lipton & Steinhardt (2018), "Troubling Trends in Machine Learning Scholarship".
- Kapoor & Narayanan (2023), "Leakage and the Reproducibility Crisis in ML-based Science".
- Henderson et al. (2018), "Deep Reinforcement Learning that Matters" — a case study in seeds and variance.

## Assignments

- **Paper-critique reps:** one structured critique per week via `/paper`, sustained for the whole program (this is the module's "problem set"). Quarterly: review a random recent arXiv paper cold and compare your review to its eventual published reviews if available.
- **Replication study:** one full replication via `/replicate`, written up with `templates/replication-report.md` — the centerpiece artifact.
- **Methodology audit:** take three published papers in your intended specialization and audit them against the pathology list above; write a memo ranking the fields' hygiene.
- **Writing reps:** a 2-page workshop-style paper on any small original result or negative result, taken through: draft → `skeptical-reviewer` agent review → rebuttal → revision.
- **Reproducibility package:** make one of your own projects rerunnable by a stranger (clean-machine test) — environment, seeds, data access, one command to regenerate every figure.

## AI study loop

- `/paper`, `/replicate`, `/lit-review`, and `/proposal` *are* this module's exercises — the skills implement its methods.
- `/advisor` weekly for planning/retrospectives; monthly for the kill-or-continue review of ongoing projects.
- Defense rehearsal: `/oral-exam` on your own written artifacts, with the examiner instructed to attack methodology rather than content knowledge.

## Mastery checklist

- [ ] Can produce a critique that identifies a genuine validity threat the authors didn't acknowledge.
- [ ] Can design an experiment with pre-committed success/failure criteria and honest statistics, and has done so.
- [ ] Can spot leakage, weak baselines, and p-hacking in others' work quickly and specifically.
- [ ] Has completed a replication whose report a stranger could rerun from a clean environment.
- [ ] Can write a related-work section that positions a contribution rather than listing citations.
- [ ] Can articulate their own taste: what makes a problem worth 12 weeks, and what kill criteria look like.
