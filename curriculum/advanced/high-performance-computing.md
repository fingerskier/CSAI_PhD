# High-Performance Computing

Extracting maximum performance from parallel hardware: the parallel programming models (shared-memory, message-passing, GPU), the performance-analysis discipline that turns intuition into measured speedup, the numerical kernels (dense/sparse linear algebra, stencils, FFT) that dominate scientific workloads, and the scaling laws and communication-avoiding algorithms that govern the largest machines. The throughline is reasoning quantitatively about parallelism, locality, and communication.

## Learning objectives

- Apply performance models — Amdahl's and Gustafson's laws, the roofline model, strong vs weak scaling — to predict and explain speedup.
- Program across the major models: shared-memory (OpenMP/threads), distributed-memory (MPI), and GPU (CUDA/SYCL), and choose the right one for a workload.
- Reason about the memory hierarchy, cache behavior, NUMA, and data locality as the dominant performance factor.
- Analyze parallel numerical kernels (BLAS/LAPACK, sparse solvers, stencils, FFT) and communication-avoiding algorithms.
- Profile and tune real code: identify bottlenecks, reason about communication/computation overlap, and validate optimizations empirically.

## Prerequisites

- [Computer Architecture](../core/computer-architecture.md) — memory hierarchy, parallelism, ILP.
- [Mathematics for CS Research](../core/math-for-cs.md) — numerical linear algebra basics.

## Primary resources

- **Pacheco & Malensek, *An Introduction to Parallel Programming*** — MPI/OpenMP foundations.
- **Hennessy & Patterson, *Computer Architecture: A Quantitative Approach*** — the quantitative mindset.
- **Berkeley CS267 (Applications of Parallel Computers)** (free online) — the spine; covers models, kernels, and scaling.
- **Kirk & Hwu, *Programming Massively Parallel Processors* (PMPP)** — GPU computing.
- **Demmel, *Applied Numerical Linear Algebra*** — the numerical-kernel foundations.

## Seminal papers

- Amdahl (1967), "Validity of the Single Processor Approach to Achieving Large-Scale Computing Capabilities."
- Gustafson (1988), "Reevaluating Amdahl's Law."
- Williams, Waterman & Patterson (2009), "Roofline: An Insightful Visual Performance Model for Multicore Architectures."
- Valiant (1990), "A Bridging Model for Parallel Computation" (BSP).
- Blumofe & Leiserson (1999), "Scheduling Multithreaded Computations by Work Stealing" (Cilk).
- Demmel et al. (2012), "Communication-Optimal Parallel and Sequential QR and LU Factorizations."
- Dongarra et al., the LINPACK/LAPACK and Top500 line of work.
- Cooley & Tukey (1965), "An Algorithm for the Machine Calculation of Complex Fourier Series" (FFT).

## Assignments

- **Problem sets:** weekly — one scaling-analysis problem, one roofline/locality analysis, one parallel-algorithm design.
- **Implementation project:** optimize a kernel (e.g. dense matrix multiply or a stencil) through blocking, vectorization, threading, and a distributed/GPU version; report the speedup at each step against the roofline.
- **Scaling study:** run strong- and weak-scaling experiments on a parallel program, identify the bottleneck (communication, load imbalance, memory), and propose+validate a fix.
- **Paper critique:** deep-read the roofline or a communication-avoiding paper via `/paper` — reconstruct the model and where its predictions break.

## AI study loop

- `/study high-performance-computing` for concept passes; predict scaling before measuring.
- `/quiz high-performance-computing` weekly — roofline reasoning and scaling laws are the highest-yield drills.
- `/oral-exam high-performance-computing`; expect "where does this lose linear speedup, and prove it with numbers."

## Mastery checklist

- [ ] Can apply Amdahl/Gustafson and distinguish strong from weak scaling.
- [ ] Can use the roofline model to classify a kernel and predict its ceiling.
- [ ] Can write correct parallel code in shared-memory, MPI, and GPU models.
- [ ] Can reason about cache/NUMA locality as the dominant performance factor.
- [ ] Can explain a communication-avoiding algorithm and why communication dominates at scale.
- [ ] Can connect the topic to current research (exascale, heterogeneous computing, performance portability, HPC–AI convergence).
