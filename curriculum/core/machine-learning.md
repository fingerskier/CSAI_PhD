# Machine Learning Foundations

Graduate ML in three layers: statistical learning theory (why learning is possible), classical methods (the pre-deep toolbox that still wins on tabular data and small samples), and deep learning (architectures, optimization, and the modern large-model stack).

## Learning objectives

- Reason with the core theory: bias–variance and approximation–estimation tradeoffs, ERM, VC dimension and Rademacher complexity, generalization bounds — and why deep learning strains classical bounds.
- Derive and implement the classical toolbox from scratch: linear/logistic regression, SVMs and kernels, decision trees and ensembles (random forests, gradient boosting), EM and mixture models, PCA.
- Build and train deep networks with full understanding of each component: backpropagation (derive it), initialization, normalization, residual connections, regularization, and the optimizer zoo (SGD/momentum/Adam).
- Explain the modern sequence stack end to end: attention, transformers, tokenization, pretraining objectives, scaling laws, fine-tuning, and RLHF/alignment basics.
- Understand reinforcement learning fundamentals: MDPs, value/policy iteration, Q-learning, policy gradients.
- Run trustworthy experiments: proper splits, leakage prevention, multiple seeds with variance, strong baselines, and ablations.

## Prerequisites

- [Mathematics for CS Research](math-for-cs.md) — especially linear algebra, probability tail bounds, and optimization. Statistics fluency is non-negotiable here.

## Primary resources

- **Bishop, *Pattern Recognition and Machine Learning*** or **Murphy, *Probabilistic Machine Learning* (2022)** — pick one as spine; Murphy is more current.
- **Hastie, Tibshirani & Friedman, *The Elements of Statistical Learning*** (free online) — classical methods at depth.
- **Shalev-Shwartz & Ben-David, *Understanding Machine Learning*** (free online) — the learning-theory layer.
- **Goodfellow, Bengio & Courville, *Deep Learning*** + **Stanford CS231n / CS224n** materials — deep learning layer.
- **Karpathy, "Neural Networks: Zero to Hero"** — build GPT from scratch; the single best implementation-pass resource.
- **Sutton & Barto, *Reinforcement Learning: An Introduction*** (free online) — chapters 1–10 for the RL unit.

## Seminal papers

- Rumelhart, Hinton & Williams (1986), "Learning Representations by Back-Propagating Errors".
- Vapnik (1999), "An Overview of Statistical Learning Theory" (or *Nature of Statistical Learning Theory* ch. 1–4).
- Krizhevsky, Sutskever & Hinton (2012), "ImageNet Classification with Deep CNNs" (AlexNet).
- He et al. (2015), "Deep Residual Learning for Image Recognition" (ResNet).
- Kingma & Ba (2014), "Adam: A Method for Stochastic Optimization" — read alongside critiques of adaptive methods.
- Vaswani et al. (2017), "Attention Is All You Need".
- Zhang et al. (2017), "Understanding Deep Learning Requires Rethinking Generalization" — the paper that broke classical bounds' grip.
- Kaplan et al. (2020), "Scaling Laws for Neural Language Models" + Hoffmann et al. (2022), "Training Compute-Optimal LLMs" (Chinchilla).
- Ouyang et al. (2022), "Training Language Models to Follow Instructions with Human Feedback" (InstructGPT/RLHF).
- Mnih et al. (2015), "Human-Level Control through Deep Reinforcement Learning" (DQN).

## Assignments

- **Problem sets:** theory problems from Shalev-Shwartz & Ben-David (VC/Rademacher) plus derivations (backprop through a full layer stack, EM for GMMs, the SVM dual).
- **From-scratch portfolio (NumPy/autograd-free where stated):** logistic regression + softmax classifier; a decision-tree/random-forest implementation; a small MLP with hand-written backprop; then a transformer language model following Zero to Hero.
- **Experiment-craft project:** pick a tabular benchmark, compare gradient boosting vs. a tuned MLP with honest methodology (CV, seeds, variance, ablations); write it up like a paper and have the `skeptical-reviewer` agent attack it.
- **Replication (Phase 2 bridge):** replicate one result from the seminal list via `/replicate` — ResNet-on-CIFAR or a scaling-law fit at small scale are well-scoped choices.

## AI study loop

- `/study machine-learning` per subtopic; always derive before importing (the attempt-first rule applies to gradients, not just proofs).
- `/quiz machine-learning` mixing theory and "debug this training run" scenario questions.
- `/paper` each seminal paper — the methodology-interrogation framing matters most for the empirical ones.

## Mastery checklist

- [ ] Can derive backpropagation for an arbitrary computation graph and implement it without a framework.
- [ ] Can state and prove a basic generalization bound (finite hypothesis class; sketch VC-based) and explain its limits for deep nets.
- [ ] Can explain every block of a transformer and the systems reasons for its design (parallelism, memory).
- [ ] Can choose between classical and deep methods for a dataset and defend the choice with evidence.
- [ ] Can design a leak-free, seed-honest experiment and detect a flawed one in a paper.
- [ ] Can connect the topic to current research (scaling laws, alignment, in-context learning theories, state-space models).
