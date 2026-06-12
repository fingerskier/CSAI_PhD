# Cloud, Edge, and Distributed Infrastructure

The systems that run modern computing at scale: virtualization and containers, resource scheduling and orchestration, the storage and coordination services that everything else builds on, serverless and edge models, and the observability and reliability engineering that keeps it all up. This is the applied counterpart to distributed-systems theory — the same consistency and fault-tolerance ideas, now under cost, multi-tenancy, and operational constraints.

## Learning objectives

- Explain virtualization and containerization (hypervisors, namespaces/cgroups, the container runtime stack) and their isolation/performance trade-offs.
- Reason about cluster scheduling and orchestration (bin-packing, fairness, Kubernetes' control-loop model) and resource isolation under multi-tenancy.
- Design scalable storage and coordination: object/blob stores, distributed file systems, and consensus-backed coordination (the applied side of Paxos/Raft).
- Compare deployment models — VMs, containers, serverless/FaaS, edge — by latency, cost, and operational complexity.
- Apply reliability engineering: SLOs/error budgets, observability (metrics/traces/logs), capacity planning, and failure-mode analysis.

## Prerequisites

- [Operating Systems](../core/operating-systems.md) — virtualization, scheduling, isolation.
- [Distributed Systems](../core/distributed-systems.md) — consensus, replication, consistency.
- Helpful: [Computer Networks](computer-networks.md) for the datacenter fabric underneath.

## Primary resources

- **Beyer et al., *Site Reliability Engineering*** (free online) — the operational/reliability spine.
- **Kleppmann, *Designing Data-Intensive Applications*** — the storage/consistency backbone (shared with databases).
- **Burns et al., *Kubernetes: Up and Running* / *Designing Distributed Systems*** — orchestration patterns.
- **Barroso, Clidaras & Hölzle, *The Datacenter as a Computer*** (free online) — warehouse-scale design.
- **The AWS / Google Cloud architecture and well-architected docs** — real-world reference designs.

## Seminal papers

GFS, MapReduce, and Dynamo reappear from [Distributed Systems](../core/distributed-systems.md) — re-read them here through the operational lens (utilization, multi-tenancy, cost) rather than the consistency lens.

- Ghemawat, Gobioff & Leung (2003), "The Google File System."
- Dean & Ghemawat (2004), "MapReduce: Simplified Data Processing on Large Clusters."
- Burrows (2006), "The Chubby Lock Service for Loosely-Coupled Distributed Systems."
- DeCandia et al. (2007), "Dynamo: Amazon's Highly Available Key-Value Store."
- Verma et al. (2015), "Large-Scale Cluster Management at Google with Borg."
- Hindman et al. (2011), "Mesos: A Platform for Fine-Grained Resource Sharing in the Data Center."
- Satyanarayanan (2017), "The Emergence of Edge Computing."
- Jonas et al. (2019), "Cloud Programming Simplified: A Berkeley View on Serverless Computing."

## Assignments

- **Problem sets:** weekly — one scheduling/bin-packing analysis, one consistency/availability trade-off case study, one capacity/SLO calculation.
- **Implementation project:** take the replicated KV store you built in [Distributed Systems](../core/distributed-systems.md) (or another non-trivial service) and productionize it — containerize it, deploy on Kubernetes with health checks, autoscaling, and observability, then add an edge-facing tier (cache/CDN or serverless function) and measure the latency and consistency consequences.
- **Reliability study:** define SLOs and an error budget for a service, design its observability, and run a failure-injection (chaos) exercise documenting how the system degrades.
- **Paper critique:** deep-read Dynamo or Borg via `/paper` — interrogate the consistency/availability or utilization/isolation trade-offs they chose.

## AI study loop

- `/study cloud-edge-infrastructure` for concept passes; reason through the trade-off before reading the design.
- `/quiz cloud-edge-infrastructure` weekly — scheduling and consistency/availability trade-offs are the highest-yield drills.
- `/oral-exam cloud-edge-infrastructure`; expect "what fails when this node dies, and what's your recovery story?"

## Mastery checklist

- [ ] Can explain container vs VM isolation and the namespace/cgroup mechanism.
- [ ] Can reason about cluster scheduling, multi-tenancy, and resource isolation.
- [ ] Can design a replicated, fault-tolerant service and justify its consistency model.
- [ ] Can compare VM/container/serverless/edge by latency, cost, and operations.
- [ ] Can define SLOs/error budgets and design observability for a service.
- [ ] Can connect the topic to current research (serverless/disaggregation, edge-cloud continuum, infrastructure for ML/LLM serving).
