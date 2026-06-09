# Distributed Systems

The theory and engineering of systems that span machines: time and ordering, fault tolerance and consensus, replication and consistency models, and the landmark industrial systems that turned the theory into infrastructure.

## Learning objectives

- Reason about time without global clocks: happens-before, Lamport and vector clocks, consistent snapshots.
- State and use the impossibility results: FLP, CAP (precisely, not as folklore), and the failure-model hierarchy (crash-stop, crash-recovery, Byzantine).
- Explain and implement consensus: Paxos and Raft in detail, leader election, log replication, reconfiguration; understand PBFT at the concept level.
- Work fluently with consistency models: linearizability, sequential consistency, causal consistency, eventual consistency — and verify a history against a model.
- Analyze the landmark systems (GFS, MapReduce, Bigtable, Dynamo, ZooKeeper, Spanner) as design points in the consistency/availability/performance space.
- Design, implement, and *test* a replicated service, including fault injection.

## Prerequisites

- [Operating Systems](operating-systems.md) (concurrency especially) and solid programming in a language with good concurrency support (Go recommended, matching 6.824).

## Primary resources

- **MIT 6.824/6.5840 (Distributed Systems)** — lectures, paper readings, and the Go lab sequence (MapReduce, Raft, KV store, sharded KV). This is the module's spine.
- **Kleppmann, *Designing Data-Intensive Applications*** — the engineering synthesis; chapters 5–9 are the heart.
- **Cachin, Guerraoui & Rodrigues, *Introduction to Reliable and Secure Distributed Programming*** — for the formal layer.
- **Jepsen analyses (jepsen.io)** — consistency claims meeting reality; read several.

## Seminal papers

- Lamport (1978), "Time, Clocks, and the Ordering of Events in a Distributed System".
- Fischer, Lynch & Paterson (1985), "Impossibility of Distributed Consensus with One Faulty Process" (FLP).
- Chandy & Lamport (1985), "Distributed Snapshots".
- Lamport (1998/2001), "The Part-Time Parliament" / "Paxos Made Simple".
- Castro & Liskov (1999), "Practical Byzantine Fault Tolerance".
- Gilbert & Lynch (2002), "Brewer's Conjecture and the Feasibility of Consistent, Available, Partition-Tolerant Web Services" (CAP, formalized).
- Ghemawat et al. (2003), "The Google File System" + Dean & Ghemawat (2004), "MapReduce".
- DeCandia et al. (2007), "Dynamo: Amazon's Highly Available Key-Value Store".
- Hunt et al. (2010), "ZooKeeper: Wait-Free Coordination for Internet-Scale Systems".
- Ongaro & Ousterhout (2014), "In Search of an Understandable Consensus Algorithm" (Raft).
- Corbett et al. (2012), "Spanner: Google's Globally-Distributed Database".

## Assignments

- **Problem sets:** weekly ordering/consistency exercises — verify histories against linearizability, construct counterexamples, vector-clock traces.
- **Implementation project (primary):** the 6.824 lab sequence through fault-tolerant Raft and the replicated key-value store. Your Raft must pass the test suite repeatedly under `-race`; flaky passes don't count.
- **Fault-injection study:** add deliberate partitions and message loss to your KV store; document every consistency violation you can provoke and why the protocol does or doesn't permit it.
- **Paper critiques:** `/paper` Dynamo vs. Spanner as a pair — two defensible opposite answers to the same question; articulate the assumptions that drive them apart.

## AI study loop

- `/study distributed-systems` per topic; for Raft, work scenario-by-scenario ("leader fails during commit — walk the message flow") rather than restating the paper.
- `/quiz distributed-systems` emphasizing failure scenarios and "is this history linearizable?" drills.
- `/oral-exam distributed-systems` — the examiner should chase precision on CAP and FLP, where folklore answers are most common.

## Mastery checklist

- [ ] Can state FLP and CAP precisely, including what each does *not* claim.
- [ ] Can implement Raft from the paper and explain every safety argument (leader completeness, log matching).
- [ ] Can determine whether a given history is linearizable and prove the verdict.
- [ ] Can place a new system on the consistency/availability/latency map from its design description.
- [ ] Can design fault-injection tests that would expose a given protocol bug.
- [ ] Can connect the topic to current research (CRDTs, deterministic databases, cloud disaggregation, Byzantine consensus in blockchains).
