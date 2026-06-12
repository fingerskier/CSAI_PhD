# Scientific Computing

The numerical methods that turn continuous mathematics into reliable computation: floating-point reality and conditioning, numerical linear algebra, solvers for differential equations, and the modeling/uncertainty pipeline that connects simulation to the physical world. The discipline is about *trustworthy* answers — knowing an algorithm's stability, error, and cost, not just that it ran.

## Learning objectives

- Reason about floating-point arithmetic, conditioning, and numerical stability; distinguish forward from backward error and analyze error propagation.
- Apply numerical linear algebra: direct and iterative solvers, least squares, eigenvalue methods, and the role of conditioning and preconditioning.
- Solve ODEs and PDEs numerically (finite difference/element/volume), and analyze stability (CFL), consistency, and convergence.
- Use numerical optimization, quadrature, interpolation, and root-finding with attention to convergence rates and cost.
- Build a credible simulation/modeling pipeline: verification, validation, and uncertainty quantification — knowing when to trust the output.

## Prerequisites

- [Mathematics for CS Research](../core/math-for-cs.md) — linear algebra, calculus, analysis.
- Helpful: [High-Performance Computing](high-performance-computing.md) for scaling the kernels.

## Primary resources

- **Trefethen & Bau, *Numerical Linear Algebra*** — the elegant, rigorous spine.
- **Heath, *Scientific Computing: An Introductory Survey*** — the broad foundations.
- **LeVeque, *Finite Difference Methods for Ordinary and Partial Differential Equations*** — the PDE/stability track.
- **Nocedal & Wright, *Numerical Optimization*** — the optimization unit.
- **MIT 18.335 (Introduction to Numerical Methods)** and **Stanford CME 302/306** — lectures and problem sets.

## Seminal papers

- Wilkinson (1961), "Error Analysis of Direct Methods of Matrix Inversion" — backward error analysis.
- Golub & Kahan (1965), "Calculating the Singular Values and Pseudo-Inverse of a Matrix."
- Courant, Friedrichs & Lewy (1928), "Über die partiellen Differenzengleichungen der mathematischen Physik" — the CFL condition.
- Hestenes & Stiefel (1952), "Methods of Conjugate Gradients for Solving Linear Systems."
- Lanczos (1950), "An Iteration Method for the Solution of the Eigenvalue Problem…"
- Saad & Schultz (1986), "GMRES: A Generalized Minimal Residual Algorithm."
- Cooley & Tukey (1965), "An Algorithm for the Machine Calculation of Complex Fourier Series" (FFT).
- Karniadakis et al. (2021), "Physics-Informed Machine Learning" — the modern ML–simulation frontier.

## Assignments

- **Problem sets:** weekly — one conditioning/stability analysis, one solver-derivation problem, one convergence-rate proof.
- **Implementation project:** implement and validate a numerical PDE solver (e.g. heat or wave equation) with a stability analysis; verify convergence against an analytic solution and demonstrate where the CFL limit bites.
- **Linear-algebra project:** implement an iterative solver (CG or GMRES) with a preconditioner; benchmark convergence vs a direct method across conditioning regimes.
- **Paper critique:** deep-read the physics-informed-ML paper via `/paper` — interrogate where learned solvers help and where classical guarantees are lost.

## AI study loop

- `/study scientific-computing` for concept passes; derive the error/stability bound before seeing it.
- `/quiz scientific-computing` weekly — conditioning/stability and convergence analysis are the highest-yield drills.
- `/oral-exam scientific-computing`; expect "what's the error, the stability condition, and the cost?"

## Mastery checklist

- [ ] Can analyze conditioning and distinguish forward from backward error.
- [ ] Can choose between direct and iterative solvers and justify it by conditioning and cost.
- [ ] Can derive a numerical scheme for an ODE/PDE and prove its stability and convergence.
- [ ] Can analyze convergence rates for optimization, quadrature, and root-finding.
- [ ] Can build a verification/validation/uncertainty-quantification argument for a simulation.
- [ ] Can connect the topic to current research (scientific ML / PINNs, differentiable simulation, randomized numerical linear algebra, mixed-precision numerics).
