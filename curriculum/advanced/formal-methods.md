# Formal Methods and Verification

Mathematically proving systems correct rather than testing them into submission: logic and decision procedures, model checking with its temporal logics and state-explosion fight, deductive verification via Hoare logic and separation logic, SMT-backed tooling, and the proof-assistant tradition where the proof *is* the artifact.

## Learning objectives

- Specify system properties precisely in temporal logic (LTL, CTL) and as pre/postcondition contracts; distinguish safety from liveness.
- Run and reason about model checking — explicit-state, symbolic (BDD), and bounded (SAT/SMT) — and the abstraction techniques (CEGAR, predicate abstraction) that fight state explosion.
- Prove programs correct with Hoare logic and separation logic, including loop invariants and reasoning about the heap and concurrency.
- Use SMT solvers as a verification backend and understand the DPLL(T) architecture and core theories.
- Construct machine-checked proofs in a proof assistant (Coq/Lean/Isabelle) and articulate the trusted computing base.

## Prerequisites

- [Theory of Computation](../core/theory-of-computation.md) — automata, decidability, logic.
- [Programming Languages and Compilers](../core/programming-languages.md) — operational semantics and type systems.

## Primary resources

- **Clarke, Grumberg, Peled et al., *Model Checking*** — the model-checking reference.
- **Pierce et al., *Software Foundations*** (free online) — Coq-based, the best on-ramp to mechanized verification.
- **Huth & Ryan, *Logic in Computer Science*** — temporal logic and proof systems.
- **Bradley & Manna, *The Calculus of Computation*** — SMT and decision procedures.
- **Appel, *Verified Functional Algorithms* / VST**, and **Concrete Semantics** (Isabelle) for the deductive track.

## Seminal papers

- Hoare (1969), "An Axiomatic Basis for Computer Programming."
- Clarke & Emerson (1981) and Queille & Sifakis (1982) — the birth of model checking (CTL).
- Pnueli (1977), "The Temporal Logic of Programs."
- Burch, Clarke, McMillan et al. (1992), "Symbolic Model Checking: 10^20 States and Beyond."
- Reynolds (2002), "Separation Logic: A Logic for Shared Mutable Data Structures."
- Biere et al. (1999), "Symbolic Model Checking without BDDs" — bounded model checking via SAT.
- Clarke, Grumberg, Jha, Lu & Veith (2000), "Counterexample-Guided Abstraction Refinement."
- Leroy (2009), "Formal Verification of a Realistic Compiler" — CompCert.
- Klein et al. (2009), "seL4: Formal Verification of an OS Kernel."

## Assignments

- **Problem sets:** weekly mixes — one temporal-logic specification, one Hoare-logic proof, one SMT-encoding exercise.
- **Implementation project:** verify a non-trivial component end-to-end — e.g. a verified data structure in Coq/Lean, or model-check a concurrency protocol (Peterson's, a lock-free queue) in TLA+/Spin and find the bug a test would miss.
- **Specification portfolio:** formalize three real informal specs (a cache-coherence rule, a security policy, an API contract) in temporal logic and discuss what the formalization exposed.
- **Paper critique:** deep-read seL4 or CompCert via `/paper` — interrogate the trusted computing base and what "verified" does and does not promise.

## AI study loop

- `/study formal-methods` for concept passes; attempt invariants and proofs before seeing them.
- `/quiz formal-methods` weekly — loop invariants and LTL/CTL semantics are the highest-yield drills.
- `/oral-exam formal-methods`; expect "what's your invariant, and why is it inductive?" and "what's in your TCB?"

## Mastery checklist

- [ ] Can specify safety and liveness properties correctly in LTL/CTL and tell them apart.
- [ ] Can find a loop invariant and complete a Hoare-logic proof for an unseen program.
- [ ] Can reason about heap and concurrency with separation logic.
- [ ] Can explain how a model checker fights state explosion (symbolic, BMC, CEGAR, abstraction).
- [ ] Can build a machine-checked proof in a proof assistant and state its trusted base.
- [ ] Can connect the topic to current research (verified systems software, SMT-based program synthesis, neural-network verification).
