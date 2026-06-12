# Cryptography and Security

Provable security from the ground up: the reduction-based definitions and proofs that distinguish cryptography from ad-hoc "security," through public-key constructions, the random-oracle debate, zero-knowledge and secure computation, and the post-quantum/lattice frontier — paired with the systems-security mindset of threat modeling and real-world attacks.

## Learning objectives

- State precise security definitions (IND-CPA/CCA, EUF-CMA, semantic security, simulation-based security) and prove constructions secure via reductions to hardness assumptions.
- Reason about the foundations: one-way functions, hardcore bits, PRGs/PRFs, and the equivalences between them.
- Construct and analyze the symmetric world — block ciphers and modes of operation, hash functions, MACs, and authenticated encryption — and explain how misuse (ECB, nonce reuse, MAC-then-encrypt) breaks it.
- Construct and analyze public-key primitives (RSA/ElGamal, elliptic-curve groups, hybrid encryption, signatures) and explain the role of the random-oracle model and its limits.
- Explain zero-knowledge proofs, commitment, secret sharing, and secure multiparty computation at the protocol level.
- Assess post-quantum cryptography — lattice problems (LWE/SIS), and the assumptions Shor's algorithm breaks.
- Threat-model real systems and reason about side channels, protocol failures, and the gap between proof and deployment.

## Prerequisites

- [Mathematics for CS Research](../core/math-for-cs.md) — number theory, probability, and reductions.
- [Theory of Computation](../core/theory-of-computation.md) — complexity classes and the reduction mindset.

## Primary resources

- **Katz & Lindell, *Introduction to Modern Cryptography*** — the definitional/provable-security spine.
- **Boneh & Shoup, *A Graduate Course in Applied Cryptography*** (free online) — modern, construction-rich.
- **Goldreich, *Foundations of Cryptography* (Vols I–II)** — for the rigorous foundations unit.
- **Dan Boneh's Coursera Cryptography** and **MIT 6.875 / Stanford CS355** — lectures and problem sets.
- **Anderson, *Security Engineering*** (free online) — the systems/threat-modeling counterweight.

## Seminal papers

- Diffie & Hellman (1976), "New Directions in Cryptography."
- Rivest, Shamir & Adleman (1978), "A Method for Obtaining Digital Signatures and Public-Key Cryptosystems."
- Goldwasser & Micali (1984), "Probabilistic Encryption" — semantic security; the definitional turn.
- Thompson (1984), "Reflections on Trusting Trust" — the systems-security counterweight in one lecture.
- Goldwasser, Micali & Rackoff (1989), "The Knowledge Complexity of Interactive Proof Systems" — zero-knowledge.
- Yao (1986), "How to Generate and Exchange Secrets" — garbled circuits / secure computation.
- Bellare & Rogaway (1993), "Random Oracles Are Practical."
- Regev (2009), "On Lattices, Learning with Errors, and Cryptography" — the LWE foundation.
- Gentry (2009), "Fully Homomorphic Encryption Using Ideal Lattices."
- Shor (1997), "Polynomial-Time Algorithms for Prime Factorization and Discrete Logarithms on a Quantum Computer."

## Assignments

- **Problem sets:** weekly reduction proofs — given a scheme and an assumption, prove security or exhibit an attack.
- **Implementation project:** implement a textbook protocol end-to-end (e.g. an authenticated-encryption scheme, or a Σ-protocol zero-knowledge proof) and write up its concrete security and pitfalls. *Never roll your own crypto for production — this is a learning artifact.*
- **Attack portfolio:** three break-the-scheme exercises (padding oracle, nonce reuse, weak-assumption forgery) with the precise definitional violation each exploits.
- **Paper critique:** deep-read Regev's LWE paper via `/paper` — trace the worst-case-to-average-case reduction and what it guarantees.

## AI study loop

- `/study cryptography-security` for concept passes; attempt each security reduction before seeing it.
- `/quiz cryptography-security` weekly — security definitions and reductions are the highest-yield drills.
- `/oral-exam cryptography-security`; expect "state the definition, then prove it" and "what assumption does this rest on?"

## Mastery checklist

- [ ] Can write a precise security definition as a game and explain the adversary's powers.
- [ ] Can prove a construction secure by reduction, accounting for the security loss.
- [ ] Can explain the random-oracle model and articulate a concrete criticism of it.
- [ ] Can choose and justify symmetric modes of operation and explain exactly what nonce reuse or a padding oracle breaks.
- [ ] Can describe a zero-knowledge or MPC protocol and argue its security properties.
- [ ] Can state LWE/SIS and explain why these underpin post-quantum schemes.
- [ ] Can connect the topic to current research (FHE, succinct proofs/zk-SNARKs, post-quantum standardization).
