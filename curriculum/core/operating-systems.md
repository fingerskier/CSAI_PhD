# Operating Systems

Graduate OS: the three pillars (virtualization, concurrency, persistence) studied through real kernels — culminating in reading and modifying a teaching kernel and engaging the research literature on OS structure.

## Learning objectives

- Explain and implement the mechanisms of virtualization: context switching, scheduling policies (MLFQ, CFS, lottery), address translation, TLBs, paging and swap, and the policy/mechanism separation.
- Reason rigorously about concurrency: locks and their hardware basis (atomics, memory ordering), condition variables and monitors, semaphores, lock-free basics, and systematic deadlock/race analysis.
- Understand persistence: the I/O stack, FFS-style file system layout, crash consistency (fsck, journaling, copy-on-write, log-structuring), and SSD/NVMe implications.
- Navigate a real kernel codebase (xv6, then targeted Linux excursions) and make non-trivial modifications.
- Engage the structural debates of the field: monolithic vs. microkernel vs. exokernel vs. unikernel; kernel-bypass; verification.

## Prerequisites

- Undergraduate OS exposure, solid C, and basic computer organization ([Computer Architecture](computer-architecture.md) can be taken concurrently).

## Primary resources

- **Arpaci-Dusseau & Arpaci-Dusseau, *Operating Systems: Three Easy Pieces* (OSTEP)** (free online) — the spine; do its homework simulators.
- **MIT 6.S081/6.1810 (Operating System Engineering)** — lectures, xv6 source, and the lab sequence (the labs are the implementation core of this module).
- **Love, *Linux Kernel Development*** — for the Linux excursions.
- **Herlihy & Shavit, *The Art of Multiprocessor Programming*** — for the concurrency unit's deeper end.

## Seminal papers

- Ritchie & Thompson (1974), "The UNIX Time-Sharing System" — the design-taste benchmark.
- Saltzer, Reed & Clark (1984), "End-to-End Arguments in System Design".
- Lampson (1983), "Hints for Computer System Design".
- Rosenblum & Ousterhout (1991), "The Design and Implementation of a Log-Structured File System".
- Engler, Kaashoek & O'Toole (1995), "Exokernel: An OS Architecture for Application-Level Resource Management".
- Anderson et al. (1992), "Scheduler Activations: Effective Kernel Support for the User-Level Management of Parallelism".
- Liedtke (1995), "On µ-Kernel Construction".
- Klein et al. (2009), "seL4: Formal Verification of an OS Kernel".
- Belay et al. (2014), "IX: A Protected Dataplane Operating System" — kernel-bypass era.

## Assignments

- **Problem sets:** OSTEP homework simulators (scheduling, VM, concurrency) weekly during the foundation pass.
- **Implementation project (primary):** the 6.S081 xv6 lab sequence — at minimum: system calls, page tables, traps, copy-on-write fork, lazy allocation, and the file-system labs. Keep an experiment log; these labs are the module's real exam.
- **Measurement project:** benchmark and explain three OS behaviors on your own machine (context-switch cost, syscall overhead, page-fault latency) — predictions first, measurements second, explanation of the gap third.
- **Paper critique:** `/paper` the exokernel paper and the seL4 paper; for each, interrogate what the claimed generality actually cost.

## AI study loop

- `/study operating-systems` for concept passes; have Claude walk xv6 source with you ("explain this trap path") rather than explaining from generalities.
- `/quiz operating-systems` emphasizing "what does the hardware do next" trace questions and crash-consistency scenarios.
- `/oral-exam operating-systems` — expect cross-examination linking schedulers to [Distributed Systems](distributed-systems.md) and page tables to [Computer Architecture](computer-architecture.md).

## Mastery checklist

- [ ] Can trace a system call, page fault, and context switch through xv6 at the source level.
- [ ] Can implement copy-on-write fork and defend its correctness under concurrency.
- [ ] Can analyze a crash-consistency protocol and state exactly what survives a crash at each step.
- [ ] Can choose and justify a locking strategy, including memory-ordering considerations.
- [ ] Can argue both sides of a kernel-structure debate with evidence from the literature.
- [ ] Can connect the topic to current research (io_uring/kernel-bypass, eBPF, verified systems, unikernels).
