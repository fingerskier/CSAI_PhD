# Computer Architecture

Quantitative computer architecture: how modern processors actually execute code (pipelines, out-of-order execution, caches, parallelism), why performance behaves the way it does, and where the field is going now that Dennard scaling and Moore's law have faded.

## Learning objectives

- Apply the quantitative method: Amdahl's law, the iron law of performance (instructions × CPI × cycle time), benchmarking pitfalls, and the roofline model.
- Explain pipelining and its hazards, branch prediction, and out-of-order execution (Tomasulo, register renaming, ROB, speculation) well enough to predict IPC behavior of real code.
- Master the memory hierarchy: cache organization and coherence (MESI), consistency models (TSO vs. relaxed and their contract with [Programming Languages](programming-languages.md) memory models), virtual memory hardware, prefetching, and DRAM realities.
- Reason about parallel hardware: multicore and synchronization cost, SIMD/vector units, and GPU execution (SIMT, warps, memory coalescing).
- Understand domain-specific acceleration: why TPUs/NPUs exist, systolic arrays, and the hardware/software co-design argument.
- Connect microarchitecture to security: why Spectre/Meltdown are *architecture* results.

## Prerequisites

- Undergraduate computer organization (single-cycle/pipelined datapath, assembly). C fluency for the measurement work.

## Primary resources

- **Hennessy & Patterson, *Computer Architecture: A Quantitative Approach* (6th ed.)** — the spine; chapters 1–5 + the DSA chapter.
- **Onur Mutlu's lectures (ETH/CMU, on YouTube)** — *Digital Design and Computer Architecture* then *Advanced Computer Architecture*; the most complete free graduate treatment.
- **Patterson & Hennessy, *Computer Organization and Design* (RISC-V ed.)** — gap-filler if the undergraduate base is shaky.
- **Drepper, "What Every Programmer Should Know About Memory"** — the memory-hierarchy unit's field guide.
- **Agner Fog's optimization manuals** + `perf`/VTune — for the measurement assignments.

## Seminal papers

- Tomasulo (1967), "An Efficient Algorithm for Exploiting Multiple Arithmetic Units".
- Patterson & Ditzel (1980), "The Case for the Reduced Instruction Set Computer".
- Smith (1981), "A Study of Branch Prediction Strategies"; Yeh & Patt (1991) on two-level adaptive prediction.
- Papamarcos & Patel (1984) on MESI-style coherence; Adve & Gharachorloo (1996), "Shared Memory Consistency Models: A Tutorial".
- Wulf & McKee (1995), "Hitting the Memory Wall".
- Esmaeilzadeh et al. (2011), "Dark Silicon and the End of Multicore Scaling".
- Williams, Waterman & Patterson (2009), "Roofline: An Insightful Visual Performance Model".
- Jouppi et al. (2017), "In-Datacenter Performance Analysis of a Tensor Processing Unit".
- Kocher et al. / Lipp et al. (2018), "Spectre Attacks" / "Meltdown".
- Hennessy & Patterson (2019), "A New Golden Age for Computer Architecture" (Turing Lecture).

## Assignments

- **Problem sets:** quantitative exercises from H&P chapters 1–5 — speedup/CPI analysis, cache and branch-predictor behavior on given code, coherence-protocol traces.
- **Measurement project (primary):** characterize your own CPU from software — measure cache sizes/latencies, branch-misprediction cost, and memory bandwidth with hand-written microbenchmarks; reconcile against published specs and explain every discrepancy.
- **Simulation project:** build a cache + branch-predictor simulator, run it on traces, and reproduce the classic miss-rate vs. size/associativity curves; or extend gem5/Ripes for one experiment.
- **Optimization case study:** take a memory-bound kernel (e.g. matmul), apply roofline analysis, then optimize stepwise (blocking, SIMD, threading) documenting predicted vs. achieved gains.
- **Paper critique:** `/paper` the TPU paper — interrogate the benchmark choices and what a fair CPU/GPU baseline means.

## AI study loop

- `/study computer-architecture` with concrete code: "why does this loop run at 0.8 IPC" beats abstract pipeline review.
- `/quiz computer-architecture` emphasizing back-of-envelope performance prediction — the examiner skill this module exists to build.
- `/oral-exam computer-architecture` — expect cross-links to OS (TLBs, context-switch cost) and ML (why GPUs/TPUs shaped the deep-learning stack).

## Mastery checklist

- [ ] Can predict within ~2× the performance of a simple kernel from first principles, then verify by measurement.
- [ ] Can trace Tomasulo/ROB execution for a code snippet and identify the bottleneck resource.
- [ ] Can explain MESI transitions and the cost model of cross-core communication.
- [ ] Can state what TSO guarantees, what it doesn't, and where fences are required.
- [ ] Can explain Spectre's mechanism and why mitigation is hard.
- [ ] Can connect the topic to current research (chiplets, CXL, processing-in-memory, open ISAs, accelerator co-design).

## Where next

[High-Performance Computing](../advanced/high-performance-computing.md) turns the quantitative method loose on parallel machines; [Deep Learning Systems](../advanced/deep-learning-systems.md) applies it to the accelerator stack the DSA chapter previews.
