# Algorithms and Complexity

Graduate-level algorithm design and analysis: the toolbox (divide and conquer, dynamic programming, greedy exchange arguments, amortization, randomization, approximation) and the limits (hardness, lower bounds, and what to do when a problem is intractable).

## Learning objectives

- Design and rigorously analyze algorithms using exchange arguments, potential functions, probabilistic analysis, and adversary arguments — not just pattern-match to known templates.
- Prove NP-hardness via reduction and respond correctly to it: approximation, parameterization, randomization, or restriction to tractable instances.
- Analyze randomized algorithms with linearity of expectation, concentration bounds (Chernoff/Azuma), and the probabilistic method.
- Work fluently with amortized analysis (aggregate, accounting, potential) and competitive analysis for online algorithms.
- Design data structures with non-obvious invariants (union-find, splay trees, persistence, succinct structures) and prove their bounds.
- Apply flow/matching/LP duality as a modeling language for combinatorial problems.

## Prerequisites

- Undergraduate algorithms (CLRS-level: asymptotics, sorting, basic graph algorithms, basic DP).
- Discrete probability and proof technique (see [Mathematics for CS Research](math-for-cs.md)).

## Primary resources

- **Kleinberg & Tardos, *Algorithm Design*** — best source for reductions and design intuition; do its exercises.
- **Erickson, *Algorithms*** (free online) — graduate-flavored coverage with excellent recursion/DP treatment.
- **CLRS, *Introduction to Algorithms*** — reference for amortization, flows, and data structures.
- **MIT 6.046J / 6.5210 (Advanced Algorithms)** — OCW lectures and problem sets; 6.5210 covers the graduate extensions (LP duality, approximation, streaming).
- **Williamson & Shmoys, *The Design of Approximation Algorithms*** (free online) — for the approximation unit.
- **Motwani & Raghavan, *Randomized Algorithms*** or Mitzenmacher & Upfal — for the randomization unit.

## Seminal papers

- Cook (1971), "The Complexity of Theorem-Proving Procedures" — NP-completeness is born.
- Karp (1972), "Reducibility Among Combinatorial Problems" — the 21 problems; the reduction style you must internalize.
- Tarjan (1975), "Efficiency of a Good But Not Linear Set Union Algorithm" — inverse-Ackermann amortized analysis.
- Sleator & Tarjan (1985), "Self-Adjusting Binary Search Trees" — splay trees, potential functions, and the dynamic-optimality conjecture.
- Karger (1993), "Global Min-Cuts in RNC" — random contraction; randomization at its most elegant.
- Indyk & Motwani (1998), "Approximate Nearest Neighbors: Towards Removing the Curse of Dimensionality" — locality-sensitive hashing.
- Spielman & Teng (2004), "Smoothed Analysis of Algorithms" — why the simplex method works in practice.
- Goemans & Williamson (1995), "Improved Approximation Algorithms for Maximum Cut…" — SDP rounding.

## Assignments

- **Problem sets:** weekly sets from 6.046/6.5210 or Erickson, timed. Mix: one reduction proof, one randomized-analysis problem, one design-from-scratch per set.
- **Implementation project:** build and benchmark three data structures with nontrivial analysis (e.g. union-find with path compression, a skip list or treap, and a splay tree); experimentally validate the amortized bounds and write up where theory and measurement diverge.
- **Hardness portfolio:** five original NP-hardness reductions for problems not in your sources, each with a correctness proof.
- **Paper critique:** deep-read Spielman & Teng via `/paper` — interrogate the model's assumptions and what "explains practice" should even mean.

## AI study loop

- `/study algorithms-complexity` for concept passes; insist on the attempt-first rule for all proofs.
- `/quiz algorithms` weekly; reductions and probabilistic analysis are the highest-yield drill categories.
- `/oral-exam algorithms-complexity` once the checklist below is mostly green — expect "prove it" follow-ups on every bound you state.

## Mastery checklist

- [ ] Can produce a correct NP-hardness reduction for an unseen problem in under an hour, with proof in both directions.
- [ ] Can analyze a randomized algorithm with Chernoff bounds and explain when union bound + concentration suffices.
- [ ] Can carry out a potential-function amortized analysis from scratch (not recite splay trees').
- [ ] Can model a problem as flow/matching/LP and use duality to certify optimality.
- [ ] Can state approximation guarantees and prove a simple ratio (e.g. 2-approx vertex cover, greedy set cover).
- [ ] Can connect the topic to current research (fine-grained complexity, smoothed analysis, learned data structures).

## Where next

[Advanced Algorithms](../advanced/advanced-algorithms.md) and [Randomized Algorithms](../advanced/randomized-algorithms.md) continue this module to the research frontier; [Cryptography and Security](../advanced/cryptography-security.md) turns hardness from an obstacle into a tool.
