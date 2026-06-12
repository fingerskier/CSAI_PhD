# Advanced Machine Learning

The theory and modern practice beyond a first ML course: statistical learning theory (what generalization *means*), kernels and the bias–variance/over-parameterization story, probabilistic and Bayesian modeling, the optimization landscape of non-convex learning, and the representation-learning paradigm that powers today's models. The goal is to reason about *why* methods work, not just call them.

## Learning objectives

- State and use generalization bounds (VC dimension, Rademacher complexity, PAC-Bayes, uniform convergence) and explain the modern puzzle they don't resolve (double descent, interpolation).
- Work fluently with kernels and the RKHS view; connect to Gaussian processes and the neural tangent kernel.
- Build probabilistic models — including graphical models and message passing — and perform approximate inference (variational inference, MCMC, the EM algorithm) with calibrated uncertainty.
- Analyze the optimization landscape of non-convex learning: SGD dynamics, implicit regularization, and why over-parameterized models generalize.
- Reason about representation learning and self-supervision as the organizing principle of modern ML.

## Prerequisites

- [Machine Learning Foundations](../core/machine-learning.md) and [Mathematics for CS Research](../core/math-for-cs.md) — probability, optimization, linear algebra.
- Comfort with convex optimization and measure-light probability.

## Primary resources

- **Shalev-Shwartz & Ben-David, *Understanding Machine Learning*** (free online) — the learning-theory spine.
- **Mohri, Rostamizadeh & Talwalkar, *Foundations of Machine Learning*** — Rademacher/margin theory.
- **Murphy, *Probabilistic Machine Learning* (Vols I–II)** — the probabilistic modeling reference.
- **Bishop, *Pattern Recognition and Machine Learning*** — kernels, EM, variational inference.
- **Rasmussen & Williams, *Gaussian Processes for Machine Learning*** (free online).
- **CMU 10-716 (Advanced ML: Theory and Methods) / Stanford STATS214 (Machine Learning Theory)** — lectures and problem sets.

## Seminal papers

- Vapnik & Chervonenkis (1971), "On the Uniform Convergence of Relative Frequencies…" — VC theory.
- Valiant (1984), "A Theory of the Learnable" — PAC learning.
- Freund & Schapire (1997), "A Decision-Theoretic Generalization of On-Line Learning" — AdaBoost and margins.
- Cortes & Vapnik (1995), "Support-Vector Networks."
- Blei, Ng & Jordan (2003), "Latent Dirichlet Allocation."
- Kingma & Welling (2014), "Auto-Encoding Variational Bayes."
- Jacot, Gabriel & Hongler (2018), "Neural Tangent Kernel."
- Zhang et al. (2017), "Understanding Deep Learning Requires Rethinking Generalization."
- Belkin et al. (2019), "Reconciling Modern Machine-Learning Practice and the Bias–Variance Trade-off" — double descent.

## Assignments

- **Problem sets:** weekly — one generalization-bound derivation, one inference derivation (EM or VI), one optimization-analysis problem.
- **Implementation project:** implement variational inference for a latent-variable model (e.g. a VAE or LDA) from scratch and study the ELBO, posterior collapse, and calibration.
- **Theory portfolio:** derive a Rademacher-complexity bound for a hypothesis class of your choice and empirically probe whether it predicts the observed generalization gap.
- **Paper critique:** deep-read Zhang et al. (2017) via `/paper` — articulate precisely why classical bounds fail to explain the result.

## AI study loop

- `/study advanced-machine-learning` for concept passes; derive bounds before seeing them.
- `/quiz advanced-machine-learning` weekly — generalization theory and approximate inference are the highest-yield drills.
- `/oral-exam advanced-machine-learning`; expect "what does this bound actually control, and does it bind in practice?"

## Mastery checklist

- [ ] Can derive a uniform-convergence / Rademacher generalization bound and state its assumptions.
- [ ] Can explain double descent and why interpolation need not overfit.
- [ ] Can derive and implement EM or variational inference for a latent-variable model.
- [ ] Can connect kernels, GPs, and the NTK as views of the same object.
- [ ] Can reason about SGD's implicit regularization in over-parameterized models.
- [ ] Can connect the topic to current research (scaling laws, in-context learning theory, mechanistic interpretability).
