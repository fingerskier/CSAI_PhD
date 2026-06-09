# Theory of Computation

Computability and complexity: what can be computed at all, what can be computed efficiently, and the great open structure of complexity classes — the module that defines the boundaries every other module works within.

## Learning objectives

- Computability: Turing machines and equivalent models, the Church–Turing thesis, universality, diagonalization, undecidability (halting problem), reductions, and Rice's theorem.
- Complexity fundamentals: time/space classes (P, NP, coNP, PSPACE, EXP, L, NL), hierarchy theorems, and complete problems for each class.
- NP-completeness deeply: Cook–Levin from the inside, the web of Karp reductions, and the practitioner consequences ([Algorithms and Complexity](algorithms-complexity.md) handles the coping strategies).
- Randomized and interactive complexity: BPP, RP, the polynomial hierarchy, IP = PSPACE, and the PCP theorem's statement and consequences for inapproximability.
- Barriers: relativization, natural proofs — why P vs. NP resists current techniques.
- Quantum computation at the literacy level: qubits, BQP, Shor's and Grover's algorithms, and what quantum does *not* promise.

## Prerequisites

- Proof maturity from [Mathematics for CS Research](math-for-cs.md); undergraduate automata/computability exposure assumed and refreshed quickly via Sipser.

## Primary resources

- **Sipser, *Introduction to the Theory of Computation*** — fast first pass (parts 1–2 review, part 3 carefully).
- **Arora & Barak, *Computational Complexity: A Modern Approach*** — the graduate spine; chapters 1–9, then selections (PCP, circuits, quantum).
- **MIT 18.404/6.5400 (Sipser's own course)** and **6.541 (Advanced Complexity)** — OCW materials.
- **Aaronson, *Quantum Computing Since Democritus*** + his lecture notes — the quantum unit, with philosophical guardrails.

## Seminal papers

- Turing (1936), "On Computable Numbers, with an Application to the Entscheidungsproblem" — read the original at least once.
- Cook (1971), "The Complexity of Theorem-Proving Procedures"; Levin (1973) for the parallel discovery.
- Karp (1972), "Reducibility Among Combinatorial Problems".
- Baker, Gill & Solovay (1975), "Relativizations of the P =? NP Question" — the first barrier.
- Shamir (1992), "IP = PSPACE".
- Arora, Lund, Motwani, Sudan & Szegedy (1998), "Proof Verification and the Hardness of Approximation Problems" — the PCP theorem (read survey treatments first).
- Razborov & Rudich (1997), "Natural Proofs" — the second barrier.
- Shor (1997), "Polynomial-Time Algorithms for Prime Factorization and Discrete Logarithms on a Quantum Computer".
- Impagliazzo (1995), "A Personal View of Average-Case Complexity" — the five worlds; the best framing essay in complexity.

## Assignments

- **Problem sets:** Sipser part 3 exercises, then Arora–Barak chapter exercises — heavy on reductions, diagonalization, and padding arguments. Timed proof attempts per the roadmap's problem pass.
- **Implementation project:** build a universal Turing machine simulator plus a reducer that mechanically converts SAT instances to 3-SAT and to CLIQUE; verify with a SAT solver on small instances.
- **Synthesis essay:** write "Impagliazzo's five worlds, ten-page tour" — explain each world, the evidence for/against, and which modern results move the needle; red-team it with the `skeptical-reviewer` agent.
- **Paper critique:** `/paper` Natural Proofs — interrogate exactly what class of proof strategies it rules out and what escapes it.

## AI study loop

- `/study theory-of-computation` — diagonalization and reduction proofs are where Socratic attempt-first discipline pays most; never accept a proof you haven't reconstructed.
- `/flashcards theory-of-computation` for class definitions, inclusions, and complete problems (the inclusion diagram should become automatic).
- `/oral-exam theory-of-computation` — expect "where exactly does this proof use the assumption?" questioning.

## Mastery checklist

- [ ] Can prove undecidability by reduction for unseen problems and state Rice's theorem precisely.
- [ ] Can sketch Cook–Levin from memory, including how the tableau encodes computation.
- [ ] Can place a new problem in the complexity zoo and justify the classification.
- [ ] Can state the hierarchy theorems and the relativization/natural-proofs barriers and what they imply about proof strategies.
- [ ] Can explain the PCP theorem's statement and derive one inapproximability consequence.
- [ ] Can connect the topic to current research (fine-grained complexity/SETH, meta-complexity, quantum supremacy claims, proof complexity).
