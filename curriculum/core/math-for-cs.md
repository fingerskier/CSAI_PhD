# Mathematics for CS Research

The working mathematical toolkit for graduate CS: linear algebra, probability and statistics, optimization, and information theory — at the level of *using* them in proofs and experiments, not just recognizing them.

## Learning objectives

- Linear algebra at the level of spectral thinking: eigendecomposition, SVD, projections, positive (semi)definiteness, matrix norms, and low-rank approximation (Eckart–Young).
- Probability at the level of tail bounds: random variables, conditioning, expectation/variance calculus, Markov/Chebyshev/Chernoff/Hoeffding, martingales and Azuma, and the probabilistic method.
- Statistics at the level of honest experiments: estimators and their bias/variance, confidence intervals, hypothesis tests and their abuse, multiple-comparison corrections, and bootstrap methods.
- Optimization at the level of reading ML papers: convexity, gradients and subgradients, Lagrangian duality and KKT, gradient descent and its convergence rates, and stochastic gradient methods.
- Information theory at the level of entropy arguments: entropy, KL divergence, mutual information, and source/channel coding intuitions.
- Proof fluency: induction (strong, structural), exchange arguments, counting (double counting, pigeonhole), and clean write-ups.

## Prerequisites

- Undergraduate calculus, linear algebra, and discrete math. This module repairs and deepens; it does not start from zero.

## Primary resources

- **Strang, *Linear Algebra and Learning from Data*** + MIT 18.06/18.065 lectures — computational/spectral viewpoint.
- **Axler, *Linear Algebra Done Right*** — the proof viewpoint; read after or alongside Strang.
- **Blitzstein & Hwang, *Introduction to Probability*** + Harvard Stat 110 lectures — probability fluency.
- **Wasserman, *All of Statistics*** — exactly the statistics a CS researcher needs, at speed.
- **Boyd & Vandenberghe, *Convex Optimization*** (free online) + Stanford EE364a — chapters 1–5 are mandatory; the rest as needed.
- **Cover & Thomas, *Elements of Information Theory*** — chapters 1–5.
- **Graham, Knuth & Patashnik, *Concrete Mathematics*** — for counting and recurrence manipulation stamina.

## Seminal papers

- Shannon (1948), "A Mathematical Theory of Communication" — read the original; it remains readable and astonishing.
- Johnson & Lindenstrauss (1984) — dimensionality reduction lemma (read a modern proof via random projections).
- Robbins & Monro (1951), "A Stochastic Approximation Method" — the ancestor of SGD.
- Cover (1965), "Geometrical and Statistical Properties of Systems of Linear Inequalities…" — capacity of linear classifiers.
- Candès, Romberg & Tao (2006), "Robust Uncertainty Principles" — compressed sensing (read for the proof style: probabilistic + spectral).
- Ioannidis (2005), "Why Most Published Research Findings Are False" — statistics as a defensive art.

## Assignments

- **Problem sets:** alternate weekly between probability/tail-bound problems (Blitzstein, MIT 6.042/6.262 sets) and optimization derivations (Boyd exercises ch. 2–5).
- **Implementation project:** implement SVD-based low-rank image compression, logistic regression by hand (gradient descent + Newton), and a bootstrap confidence-interval study on a real dataset; verify each against library implementations.
- **Proof portfolio:** ten polished proofs spanning induction, exchange, probabilistic method, and a convexity/duality argument; graded on rigor and clarity via `/quiz` rubrics.
- **Statistics audit:** take one published ML paper and audit its statistical claims (variance reporting, seed counts, significance) — write a one-page memo.

## AI study loop

- `/study math-for-cs` with explicit subtopic (e.g. "/study Chernoff bounds") — three-pass explanations (intuition, formalism, implementation) work especially well here.
- `/flashcards math-for-cs` — definitions, theorem statements, and bound forms are ideal card material; proof *sketches* get their own cards.
- 21-day recall rule from the roadmap: re-derive one major inequality from scratch every three weeks.

## Mastery checklist

- [ ] Can derive and apply Chernoff/Hoeffding bounds to a new problem without references.
- [ ] Can compute/reason about SVD, eigenvalues, and PSD-ness, and explain Eckart–Young.
- [ ] Can set up a Lagrangian, derive KKT conditions, and interpret the dual for a simple problem.
- [ ] Can design an experiment with correct statistical reporting and spot p-hacking in others'.
- [ ] Can use entropy/KL/mutual information correctly in an argument (e.g. lower bounds, loss functions).
- [ ] Can connect the topic to current research (e.g. why Adam ≠ SGD convergence theory, conformal prediction, matrix concentration in deep learning theory).

## Where next

The probability toolkit sharpens into [Randomized Algorithms](../advanced/randomized-algorithms.md), the statistics and optimization feed [Advanced Machine Learning](../advanced/advanced-machine-learning.md), and the numerical linear algebra grows into [Scientific Computing](../advanced/scientific-computing.md).
