# Databases and Data-Intensive Systems

Database internals and the architecture of data systems: storage engines, query processing and optimization, transactions and recovery, and the modern landscape (columnar analytics, distributed OLTP, lakehouse).

## Learning objectives

- Explain the relational model and its theory: relational algebra, normalization, and why declarativity is the field's central bet.
- Understand storage engines deeply: page layout, buffer management, B+trees vs. LSM-trees and their read/write/space amplification tradeoffs.
- Trace query execution end to end: parsing, logical/physical plans, the iterator (Volcano) model vs. vectorized execution, join algorithms, and cost-based optimization (Selinger-style).
- Master transactions: ACID precisely, serializability theory, two-phase locking, MVCC, optimistic concurrency control, isolation levels and their anomalies, and ARIES-style recovery.
- Analyze modern architectures: column stores, shared-nothing vs. disaggregated storage, HTAP, and streaming systems.
- Use the theory to predict and measure real engine behavior (PostgreSQL, SQLite, RocksDB).

## Prerequisites

- [Operating Systems](operating-systems.md) (storage stack, concurrency) and comfort with C/C++ or Rust for the implementation project.

## Primary resources

- **CMU 15-445/645 (Database Systems, Pavlo)** — lectures and the BusTub project sequence; the module's spine.
- **Hellerstein & Stonebraker (eds.), *Readings in Database Systems* ("Red Book", 5th ed.)** (free online) — curated papers with commentary.
- **Kleppmann, *Designing Data-Intensive Applications*** — chapters 1–4 and 7 for this module (5–9 belong to [Distributed Systems](distributed-systems.md)).
- **CMU 15-721 (Advanced Database Systems)** — for the modern-architecture unit.

## Seminal papers

- Codd (1970), "A Relational Model of Data for Large Shared Data Banks".
- Selinger et al. (1979), "Access Path Selection in a Relational Database Management System" — still the optimizer blueprint.
- Gray et al. (1976/1981) on granularity of locks and transaction concepts; Gray (1981), "The Transaction Concept: Virtues and Limitations".
- Mohan et al. (1992), "ARIES: A Transaction Recovery Method Supporting Fine-Granularity Locking…".
- Graefe (1994), "Volcano — An Extensible and Parallel Query Evaluation System".
- O'Neil et al. (1996), "The Log-Structured Merge-Tree (LSM-Tree)".
- Stonebraker et al. (2005), "C-Store: A Column-oriented DBMS".
- Berenson et al. (1995), "A Critique of ANSI SQL Isolation Levels".
- Diaconu et al. (2013), "Hekaton: SQL Server's Memory-Optimized OLTP Engine".
- Dageville et al. (2016), "The Snowflake Elastic Data Warehouse".
- Stonebraker & Hellerstein, "What Goes Around Comes Around" — read first and last; it frames the whole module.

## Assignments

- **Problem sets:** relational algebra/SQL equivalence proofs, join cost estimation, serializability testing (conflict graphs), and isolation-anomaly construction.
- **Implementation project (primary):** the 15-445 BusTub sequence — buffer pool manager, B+tree (or hash) index, query executors with optimizer rules, and lock-manager/MVCC concurrency control.
- **Measurement project:** design experiments that expose engine internals from the outside — e.g. detect PostgreSQL's plan changes as table stats shift; measure RocksDB write amplification under different compaction settings. Predict, measure, explain.
- **Paper critique:** `/paper` "What Goes Around Comes Around" and write your own position on which current trend (vector DBs, lakehouse, HTAP) it would predict to fold back into the relational model.

## AI study loop

- `/study databases` per layer (storage → execution → transactions); use real `EXPLAIN ANALYZE` output as study material.
- `/quiz databases` emphasizing isolation anomalies, cost estimation, and recovery traces ("crash here — replay the log").
- `/oral-exam databases` — expect cross-links to OS (buffer pool vs. page cache) and distributed systems (commit protocols).

## Mastery checklist

- [ ] Can implement a buffer pool and B+tree and explain every latch/lock decision.
- [ ] Can hand-derive a Selinger-style plan for a 3-way join and predict what a real optimizer picks.
- [ ] Can name the anomaly each isolation level permits and construct a schedule exhibiting it.
- [ ] Can walk ARIES recovery (analysis/redo/undo) over a concrete log.
- [ ] Can argue row-store vs. column-store vs. LSM for a workload with amplification numbers.
- [ ] Can connect the topic to current research (learned indexes/optimizers, disaggregation, vector search, streaming SQL).
