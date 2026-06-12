# Advanced Algorithms

Modern algorithmic paradigms past the core toolbox: spectral and continuous methods, sublinear/streaming algorithms, advanced approximation via LP/SDP rounding, online and competitive analysis at depth, and the fine-grained complexity that explains why some "polynomial" problems resist speedup. The throughline: when classical worst-case design stalls, change the resource (space, randomness, queries) or the relaxation.

## Learning objectives

- Design sublinear-time and streaming algorithms and prove their space/approximation trade-offs via sketching and frequency-moment lower bounds.
- Use spectral methods — graph Laplacians, eigenvalue/conductance (Cheeger) connections, and nearly-linear-time Laplacian solvers — as a design language for cuts, clustering, and flows.
- Round LP and SDP relaxations (deterministic, randomized, primal-dual, iterative) and certify integrality gaps.
- Analyze online algorithms with potential functions, the primal-dual framework, and randomized lower bounds against adaptive adversaries.
- Place "easy" problems in the fine-grained hierarchy (3SUM, APSP, OV) and derive conditional lower bounds via reductions from SETH.

## Prerequisites

- [Algorithms and Complexity](../core/algorithms-complexity.md) — reductions, randomized analysis, LP duality, approximation basics.
- Linear algebra and spectral theory (see [Mathematics for CS Research](../core/math-for-cs.md)); comfort with probabilistic concentration.
- Note: the core module already touched 6.5210 and basic approximation (Goemans–Williamson, LSH) — skip what you've mastered; the new ground here is streaming, spectral methods, online primal-dual, and fine-grained complexity.

## Primary resources

- **MIT 6.5210 / 6.854 (Advanced Algorithms)** — Karger's lectures and problem sets; the spine of this module.
- **Williamson & Shmoys, *The Design of Approximation Algorithms*** (free online) — LP/SDP rounding and primal-dual.
- **Spielman, *Spectral and Algebraic Graph Theory*** (free online) — Laplacians, expanders, Cheeger.
- **Roughgarden, *Beyond the Worst-Case Analysis of Algorithms*** — smoothed/semi-random models and online competitiveness.
- **McGregor / Muthukrishnan, *Data Streams* surveys** — the streaming canon.
- **Borodin & El-Yaniv, *Online Computation and Competitive Analysis***.

## Seminal papers

- Alon, Matias & Szegedy (1999), "The Space Complexity of Approximating the Frequency Moments" — the streaming model and its lower bounds.
- Spielman & Teng (2011), "Spectral Sparsification of Graphs" (and the 2004 nearly-linear Laplacian solver work).
- Cheeger (1970) / Alon–Milman (1985) — the conductance–eigenvalue inequality (read via Spielman's notes).
- Goemans & Williamson (1995), "Improved Approximation Algorithms for Maximum Cut and Satisfiability Problems Using Semidefinite Programming."
- Arora, Rao & Vazirani (2009), "Expander Flows, Geometric Embeddings and Graph Partitioning."
- Karp, Vazirani & Vazirani (1990), "An Optimal Algorithm for On-Line Bipartite Matching."
- Williams (2005), "A New Algorithm for Optimal 2-Constraint Satisfaction and Its Implications" — fine-grained reductions.
- Indyk & Motwani (1998), "Approximate Nearest Neighbors" — LSH, sketching for high dimensions.
- Bansal, Buchbinder & Naor (2007), "A Primal-Dual Randomized Algorithm for Weighted Paging."

## Assignments

- **Problem sets:** weekly 6.854/6.5210 sets — at least one streaming, one rounding, and one online problem per set.
- **Implementation project:** implement a Count-Min / AMS sketch and a spectral clustering pipeline; empirically measure space–accuracy trade-offs against exact baselines and write up where the bounds bind.
- **Rounding portfolio:** three relaxation-and-rounding analyses (one LP, one SDP, one primal-dual) with proved approximation ratios and a matching integrality-gap instance for one of them.
- **Paper critique:** deep-read ARV via `/paper` — interrogate the metric embedding step and what the √(log n) barrier actually buys.

## AI study loop

- `/study advanced-algorithms` for concept passes; enforce attempt-first on every bound.
- `/quiz advanced-algorithms` weekly — streaming lower bounds and SDP rounding are the highest-yield drills.
- `/oral-exam advanced-algorithms` once the checklist is mostly green; expect "what's the lower bound, and is it tight?" on everything.

## Mastery checklist

- [ ] Can derive a streaming space lower bound via a communication-complexity reduction.
- [ ] Can state and prove a Cheeger-type bound and explain its algorithmic consequence.
- [ ] Can round an SDP relaxation and prove the resulting approximation ratio.
- [ ] Can give a primal-dual analysis of an online algorithm with a competitive-ratio proof.
- [ ] Can place a problem in the fine-grained landscape and reduce from SETH/OV/3SUM/APSP.
- [ ] Can connect the topic to current research (dynamic graph algorithms, learning-augmented algorithms, continuous optimization for combinatorial problems).
