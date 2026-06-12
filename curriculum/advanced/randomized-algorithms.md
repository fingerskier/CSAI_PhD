# Randomized Algorithms

Randomness as a first-class algorithmic resource: the probabilistic method, concentration, random walks and the spectral view of mixing, hashing and dimensionality reduction, Markov-chain Monte Carlo, and the derandomization machinery (pairwise independence, expanders, the method of conditional expectations) that asks how much randomness an algorithm truly needs.

## Learning objectives

- Apply the probabilistic method (first/second moment, Lovász Local Lemma, and its algorithmic Moser–Tardos form) to prove existence and to construct.
- Prove sharp concentration with Chernoff/Hoeffding, Azuma martingale bounds, and bounded-differences (McDiarmid), and know which tool the dependence structure demands.
- Analyze Markov chains via coupling, conductance, and spectral gap; bound mixing times and design MCMC samplers.
- Use limited independence, universal/perfect hashing, and the JL lemma; explain the randomness–performance trade-off.
- Derandomize via conditional expectations, pairwise independence, and expander walks; situate BPP vs P.

## Prerequisites

- [Algorithms and Complexity](../core/algorithms-complexity.md) and [Mathematics for CS Research](../core/math-for-cs.md) — discrete probability, linear algebra, proof technique.
- Comfort with eigenvalues and basic measure-free probability.
- Note: core covered linearity of expectation, basic Chernoff, and Karger's min-cut — this module assumes them and goes deeper (LLL, mixing times, derandomization).

## Primary resources

- **Mitzenmacher & Upfal, *Probability and Computing*** — the primary text; do its exercises.
- **Motwani & Raghavan, *Randomized Algorithms*** — the classical reference for derandomization and game-theoretic lower bounds.
- **Alon & Spencer, *The Probabilistic Method*** — for the existence-proof unit.
- **Levin & Peres, *Markov Chains and Mixing Times*** (free online) — coupling and conductance.
- **MIT 6.856 / CMU 15-859 Randomized Algorithms** — lectures and problem sets.

## Seminal papers

- Karger (1993), "Global Min-Cuts in RNC" — random contraction.
- Schöning (1999), "A Probabilistic Algorithm for k-SAT" — the random-walk SAT bound.
- Moser & Tardos (2010), "A Constructive Proof of the General Lovász Local Lemma."
- Johnson & Lindenstrauss (1984), "Extensions of Lipschitz Mappings into a Hilbert Space" — dimensionality reduction.
- Jerrum, Sinclair & Vigoda (2004), "A Polynomial-Time Approximation Algorithm for the Permanent" — MCMC at its peak.
- Carter & Wegman (1979), "Universal Classes of Hash Functions."
- Spencer (1985), "Six Standard Deviations Suffice" — the partial-coloring/discrepancy method.
- Valiant & Vazirani (1986), "NP Is as Easy as Detecting Unique Solutions" — isolation via randomness.

## Assignments

- **Problem sets:** weekly sets mixing one concentration proof, one probabilistic-method construction, and one Markov-chain mixing bound.
- **Implementation project:** build an MCMC sampler (e.g. Gibbs for the Ising model or approximate counting of matchings); empirically estimate mixing time and compare to the conductance bound.
- **Derandomization study:** take two randomized algorithms and derandomize one via conditional expectations and one via pairwise independence, with full analysis.
- **Paper critique:** deep-read Moser–Tardos via `/paper` — reconstruct the entropy-compression argument in your own words.

## AI study loop

- `/study randomized-algorithms` for concept passes; attempt every concentration bound before seeing it.
- `/quiz randomized-algorithms` weekly — concentration and the probabilistic method are the core drills.
- `/oral-exam randomized-algorithms`; expect "why this tail bound and not that one?" and "now remove the randomness."

## Mastery checklist

- [ ] Can choose and correctly apply the right concentration inequality given the dependence structure.
- [ ] Can carry out a second-moment or LLL existence proof for an unseen problem.
- [ ] Can bound a Markov chain's mixing time via coupling or conductance.
- [ ] Can apply the JL lemma and state its dimension dependence.
- [ ] Can derandomize an algorithm two distinct ways and state the cost.
- [ ] Can connect the topic to current research (high-dimensional expanders, discrepancy theory, randomized numerical linear algebra).
