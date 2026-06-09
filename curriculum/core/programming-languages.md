# Programming Languages and Compilers

Two intertwined tracks: the *theory* of languages (semantics, type systems, verification) and the *engineering* of compilers (parsing through optimization and code generation), each culminating in building working artifacts.

## Learning objectives

- Define languages formally: operational semantics (small/big-step), and reading denotational and axiomatic (Hoare logic) definitions.
- Work with type systems as proof systems: simply-typed lambda calculus, progress + preservation proofs, polymorphism (System F), algebraic data types, and Hindley–Milner type inference.
- Understand what types buy: memory safety, data-race freedom (Rust's ownership/borrowing as an affine-type system), and the Curry–Howard view.
- Build a complete compiler: lexing/parsing, semantic analysis, intermediate representations (SSA), classic optimizations (constant propagation, CSE, inlining, loop transforms), register allocation, and code generation.
- Understand garbage collection (mark-sweep, copying, generational) and runtime systems (closures, dispatch, JIT basics).
- Evaluate language-design claims empirically and historically — what made ML, Lisp, and Rust's ideas survive.

## Prerequisites

- [Theory of Computation](theory-of-computation.md) helps (grammars, decidability) but can run concurrently. Functional-programming exposure (any ML-family language or Haskell) is needed for the theory track.

## Primary resources

- **Pierce, *Types and Programming Languages* (TAPL)** — the theory spine; chapters 1–15 + 22–24 minimum.
- **Harper, *Practical Foundations for Programming Languages* (PFPL)** (free draft online) — second pass on theory, broader and terser.
- **Nystrom, *Crafting Interpreters*** (free online) — the on-ramp: build a tree-walker and a bytecode VM.
- **Cooper & Torczon, *Engineering a Compiler*** (or Appel's *Modern Compiler Implementation in ML*) — the compiler-engineering spine.
- **Software Foundations (Pierce et al.)** vol. 1–2 — optional but transformative: mechanized proofs in Coq/Rocq.

## Seminal papers

- Landin (1966), "The Next 700 Programming Languages".
- Hoare (1969), "An Axiomatic Basis for Computer Programming".
- Milner (1978), "A Theory of Type Polymorphism in Programming" — Hindley–Milner inference.
- Reynolds (1983), "Types, Abstraction and Parametric Polymorphism" — "theorems for free" foundations.
- Cytron et al. (1991), "Efficiently Computing Static Single Assignment Form…" — SSA.
- Lattner & Adve (2004), "LLVM: A Compilation Framework for Lifelong Program Analysis & Transformation".
- Jim et al. (2002), "Cyclone: A Safe Dialect of C" + Matsakis & Klock (2014), "The Rust Language" — the lineage of ownership types.
- Siek & Taha (2006), "Gradual Typing for Functional Languages".
- Leroy (2009), "Formal Verification of a Realistic Compiler" (CompCert).

## Assignments

- **Problem sets:** TAPL exercises — especially progress/preservation proofs for STLC plus one extension (references or exceptions) done fully.
- **Implementation project 1:** Crafting Interpreters both halves (tree-walking interpreter, then bytecode VM with GC).
- **Implementation project 2 (primary):** a compiler for a small typed language to a real target (x86-64, RISC-V, or WASM) with an SSA-based IR and at least three optimization passes; benchmark the passes and report measured (not assumed) wins.
- **Type-system mini-project:** implement Hindley–Milner inference for a mini-ML, with let-polymorphism and an occurs-check; property-test it against hand-derived typings.
- **Paper critique:** `/paper` CompCert — interrogate what "verified" does and doesn't cover (the trusted base, the spec gap).

## AI study loop

- `/study programming-languages` — for proofs, the Socratic attempt-first rule is essential; for compiler passes, study with real IR dumps (`llvm -O1 -print-after-all` style) as material.
- `/quiz programming-languages` mixing typing-derivation drills with "what does this optimization break" scenario questions.
- `/oral-exam programming-languages` — expect to defend a language-design tradeoff (e.g. gradual typing's soundness costs) end to end.

## Mastery checklist

- [ ] Can write small-step semantics and a progress/preservation proof for an extended STLC.
- [ ] Can execute Hindley–Milner inference by hand and explain where it breaks (polymorphic recursion, higher-rank types).
- [ ] Can explain Rust's borrow checker in type-theoretic terms and what it cannot express.
- [ ] Can build a working optimizing compiler and demonstrate each pass's effect on real code.
- [ ] Can compare GC strategies with workload-dependent tradeoffs, not slogans.
- [ ] Can connect the topic to current research (verification at scale, effect systems, ML-for-compilers, WASM as a universal target).
