# Responsible Computing, Ethics, and Research Risk

The normative and practical obligations of CS research: privacy, security, fairness, safety, human subjects, dual use, environmental cost, and governance. The goal is not a generic ethics essay; it is the ability to identify stakeholders, harms, threat models, and mitigations that materially affect research design.

## Learning objectives

- Identify stakeholders, affected communities, incentives, and failure modes for a proposed system or study.
- Analyze privacy and security risks using threat models, data-flow maps, consent boundaries, and disclosure plans.
- Evaluate fairness and representational harms in datasets, models, interfaces, and benchmarks.
- Reason about dual-use and misuse risk for AI, security, bio/cyber-physical, and data-mining work.
- Apply human-subjects and research-integrity norms: consent, IRB-style review, deception, data retention, authorship, conflicts of interest, and responsible disclosure.
- Include environmental and labor costs in system and ML evaluation when they are material.

## Prerequisites

- [Research Methods](research-methods.md) for paper critique and proposal writing.
- Basic security/privacy vocabulary from [Cryptography and Security](../advanced/cryptography-security.md) is helpful but not required.

## Primary resources

- **ACM Code of Ethics and Professional Conduct** — baseline professional obligations.
- **Belmont Report** and **Menlo Report** — human-subjects and ICT research ethics.
- **NIST AI Risk Management Framework** — practical structure for AI risk identification and mitigation.
- **Barocas, Hardt & Narayanan, *Fairness and Machine Learning*** — technical and social foundations of fairness.
- **D'Ignazio & Klein, *Data Feminism*** — data power, collection, and interpretation.
- **Solove, *Understanding Privacy*** or selected privacy taxonomy readings.

## Seminal papers and reports

- Friedman & Nissenbaum (1996), "Bias in Computer Systems."
- Sweeney (2002), "k-Anonymity: A Model for Protecting Privacy."
- Narayanan & Shmatikov (2008), "Robust De-anonymization of Large Sparse Datasets."
- Dwork et al. (2012), "Fairness Through Awareness."
- Mitchell et al. (2019), "Model Cards for Model Reporting."
- Gebru et al. (2021), "Datasheets for Datasets."
- Bender et al. (2021), "On the Dangers of Stochastic Parrots."
- Weidinger et al. (2021), "Ethical and Social Risks of Harm from Language Models."
- Strubell, Ganesh & McCallum (2019), "Energy and Policy Considerations for Deep Learning in NLP."

## Assignments

- **Risk register:** for one project, create a living table of stakeholders, harms, likelihood, severity, detection signals, mitigations, and owners.
- **Dataset/system card:** write a datasheet, model card, or system card for an artifact you build or replicate.
- **Threat model:** map assets, adversaries, entry points, abuse cases, and responsible-disclosure obligations for a data or AI system.
- **Paper critique:** choose a paper from your specialization and write the ethics section reviewers wish it had: limitations, misuse, privacy, fairness, environmental cost, and deployment assumptions.
- **Governance memo:** write a one-page go/no-go recommendation for releasing a model, dataset, benchmark, or tool.

## AI study loop

- `/study responsible-computing` for frameworks, but require concrete stakeholders and system boundaries before discussing principles.
- `/paper <paper>` with the instruction: add a risk register and identify missing consent, privacy, fairness, or misuse analysis.
- `/proposal <idea>` with red-team focus on misuse, externalities, human-subjects concerns, and release criteria.
- `/oral-exam responsible-computing` — expect committee-style pressure on tradeoffs and whether mitigations are operational.

## Mastery checklist

- [ ] Can produce a concrete stakeholder and harm analysis for a research idea.
- [ ] Can threat-model data collection, model release, benchmark publication, or system deployment.
- [ ] Can identify common fairness, privacy, consent, and dual-use failures in CS papers.
- [ ] Can write artifact documentation that states intended use, out-of-scope use, limitations, and evaluation gaps.
- [ ] Can propose mitigations with measurable triggers rather than vague assurances.
- [ ] Can defend a release, withhold, or staged-access decision under adversarial questioning.

## Where next

Use this module as a cross-cutting requirement for all proposals, replications, and capstones. It pairs especially with [Natural Language Processing](../advanced/natural-language-processing.md), [Computer Vision](../advanced/computer-vision.md), [Human-Computer Interaction](../advanced/human-computer-interaction.md), [Cryptography and Security](../advanced/cryptography-security.md), [Robotics and Control](../advanced/robotics-control.md), and [Cloud, Edge, and Distributed Infrastructure](../advanced/cloud-edge-infrastructure.md).
