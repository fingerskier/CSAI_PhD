# Program Roadmap

This roadmap expands each phase with concrete execution details, emphasizing **AI-assisted study, reinforcement, and evaluation**. Use it as your operational guide for weekly planning, daily prompts, and milestone readiness checks.

## How to run each week (all phases)

1. **Plan (30–45 min):** define weekly objectives, outputs, and constraints.
2. **Study (6–12 hrs):** deep work on theory, implementation, and paper reading.
3. **Reinforce (2–4 hrs):** retrieval practice, spaced repetition, and error correction.
4. **Evaluate (1–2 hrs):** produce evidence of mastery via written/technical artifacts.
5. **Retrospective (30 min):** calibrate what to continue, stop, and redesign.

### AI-assisted workflow pattern

For every module, run a repeating loop:

- **Explain:** ask AI to explain a concept at 3 levels (intuitive, formal, implementation).
- **Generate:** request targeted exercises at increasing difficulty.
- **Attempt first:** solve before looking at hints.
- **Critique:** submit your solution and ask AI for rubric-based scoring.
- **Repair:** create an error log and re-attempt variants 48 hours later.
- **Transfer:** apply the same concept in a new domain (e.g., from NLP to systems).

### Prompt bank (core templates)

- **Concept breakdown:**
  - “Teach me `<topic>` in three passes: intuition, formalism, and practical implementation. Include common misconceptions and edge cases.”
- **Socratic coaching:**
  - “Do not give final answers yet. Ask me one question at a time so I derive `<topic/proof/solution>` myself.”
- **Problem generation:**
  - “Generate 5 graduate-level problems on `<topic>`: 2 conceptual, 2 quantitative, 1 open-ended. Provide hidden rubric and release hints only on request.”
- **Solution critique:**
  - “Grade my solution using this rubric: correctness (40), depth (25), rigor (20), clarity (15). Identify the minimum changes needed for full marks.”
- **Research paper digestion:**
  - “Interrogate this paper: assumptions, novelty, baselines, threats to validity, reproducibility gaps, and strongest follow-up experiments.”
- **Oral exam simulation:**
  - “Run a 15-minute oral defense on `<topic>`. Start broad, then progressively probe failure modes and tradeoffs.”

### Evaluation standards (all phases)

Use these thresholds before advancing:

- **Mastery threshold:** ≥85% average on self-tests across 3 spaced attempts.
- **Transfer threshold:** successful application in at least 2 novel contexts.
- **Communication threshold:** explain concept in ≤5 minutes with formal precision.
- **Artifact threshold:** produce reproducible notes/code/results another person can run.

---

## Phase 0: Diagnostic and setup

**Duration:** 1–2 months

### Objectives

- Identify gaps in math, programming, systems, algorithms, and statistics.
- Set up research workflow: bibliography manager, note system, experiment tracking, version control.
- Choose preliminary specialization interests.
- Establish AI study infrastructure (prompt library, evaluation rubrics, revision cadence).

### Weekly execution

- Run one diagnostic domain per week (math, algorithms, systems, ML, research methods).
- For each weak area, create:
  - 10-question competency check,
  - 2 implementation drills,
  - 1 short teaching note (“explain to a first-year grad student”).

### AI prompts for Phase 0

- “Create a diagnostic test for `<domain>` with answer key and skill tags.”
- “Given my incorrect answers, infer my prerequisite gaps and propose a 4-week repair plan.”
- “Turn my gaps into a spaced-repetition deck with increasing difficulty.”

### Deliverables

- Completed diagnostic assessment.
- Personal study plan with weekly schedule.
- Initial reading queue of 25–50 papers.
- Prompt/rubric starter kit for all subsequent phases.

### Exit criteria

- Baseline competency map completed.
- Weekly routine is sustainable for 3 consecutive weeks.
- Priority gaps ranked and sequenced with measurable targets.

---

## Phase 1: Graduate CS core

**Duration:** 9–12 months

### Core areas

- Algorithms and complexity
- Probability, statistics, and optimization
- Machine learning foundations
- Operating systems and distributed systems
- Databases and data-intensive systems
- Programming languages and compilers
- Computer architecture
- Theory of computation

### Execution model by module

For each core module:

1. **Foundation pass:** textbook + lecture coverage map.
2. **Problem pass:** weekly proof/problem sets with timed attempts.
3. **Build pass:** one implementation mini-project.
4. **Defense pass:** oral exam simulation and written synthesis.

### AI prompts for Phase 1

- “Generate a 12-week graduate syllabus for `<module>` with weekly checkpoints and cumulative assessments.”
- “Create a mixed set of theorem-proof and implementation questions; adapt difficulty based on my last score.”
- “Evaluate this code for algorithmic complexity, correctness edge cases, and experimental validation quality.”

### Reinforcement protocol

- 24-hour recall: summarize from memory without notes.
- 7-day recall: re-solve one old problem under time pressure.
- 21-day recall: teach the topic and answer adversarial questions.

### Deliverables

- Course notes for each core module.
- 6–10 substantial programming assignments or mini-projects.
- Breadth exam covering core areas.

### Exit criteria

- ≥85% breadth readiness on three timed mixed-domain mocks.
- At least one strong artifact per core area (proof set, project, or report).
- Demonstrated ability to connect at least 3 areas (e.g., systems ↔ ML ↔ optimization).

---

## Phase 2: Advanced topics and research literacy

**Duration:** 9–12 months

### Objectives

- Read 75–150 research papers.
- Reproduce 2–3 important papers.
- Write critical surveys in at least two areas.
- Practice seminar-style presentations.

### Reading-to-research pipeline

- **Triage:** title/abstract/method scan (10–15 min).
- **Deep read:** claim-evidence map, assumptions, limitations.
- **Reproduce:** rerun core experiment or derive key theorem/argument.
- **Extend:** propose one modification and expected outcome.

### AI prompts for Phase 2

- “Convert this paper into a reproducibility checklist with required artifacts, expected metrics, and risk points.”
- “Stress-test the paper: where could confounding variables or leakage occur?”
- “Act as a skeptical reviewer and write 5 major + 5 minor comments.”

### Evaluation rubric (paper work)

- Correctness of interpretation.
- Depth of critique.
- Reproduction fidelity.
- Quality of extension hypothesis.
- Clarity of communication.

### Deliverables

- Literature survey.
- Replication reports.
- Advanced project portfolio.

### Exit criteria

- Replications independently reproducible from clean environment.
- Survey identifies concrete open problems with tractable scopes.
- Seminar presentation can withstand cross-examination on methods/assumptions.

---

## Phase 3: Specialization and original research

**Duration:** 12–18 months

### Objectives

- Select primary research area.
- Define open problems.
- Build research prototypes.
- Submit workshop-style papers or technical reports.

### Research operating cycle

1. Problem framing and literature delta.
2. Hypothesis and success/failure criteria.
3. Experiment/system design.
4. Implementation and ablation analysis.
5. Write-up and external feedback.

### AI prompts for Phase 3

- “Given this literature map, identify underexplored problem slices with high research value and feasible scope in 12 weeks.”
- “Create ablation and robustness plans that could falsify my hypothesis.”
- “Red-team my methodology for leakage, p-hacking, benchmark overfitting, and weak baselines.”

### Reinforcement focus

- Weekly “defense rehearsal” with adversarial questioning.
- Monthly retrospective on failed hypotheses and what was learned.
- Continuous experiment log normalization for reproducibility.

### Deliverables

- Research proposal.
- 1–2 original research projects.
- Public artifact: code, dataset, benchmark, or system.

### Exit criteria

- At least one project with clear novel contribution claim.
- Evidence package supports claims (ablations, error analysis, limits).
- External technical feedback integrated into revised manuscript.

---

## Phase 4: Dissertation-style capstone

**Duration:** 12–24 months

### Objectives

- Execute a coherent research agenda.
- Produce multiple paper-length chapters.
- Defend claims with theory, experiments, or system evidence.

### Capstone structure

- **Chapter 1:** problem framing + motivation + literature synthesis.
- **Chapter 2+:** individual contributions (method/system/theory).
- **Final chapter:** synthesis, limitations, future research agenda.

### AI prompts for Phase 4

- “Challenge my thesis narrative coherence: do chapters logically compose into one central claim?”
- “Identify the weakest evidence chain and propose the highest-leverage experiment to strengthen it.”
- “Run a mock defense committee: each examiner asks 5 domain-specific questions.”

### Evaluation for defense readiness

- Claim-evidence traceability is explicit and testable.
- All figures/tables reproducible from scripts.
- Limitations and negative results are documented and defended.
- Oral defense consistently clear under interruption and critique.

### Deliverables

- Dissertation-style manuscript.
- Defense presentation.
- Reproducible research package.

### Exit criteria

- Full manuscript passes internal rubric review.
- Mock defense reaches passing consensus.
- Reproducibility check succeeds on a clean setup.
