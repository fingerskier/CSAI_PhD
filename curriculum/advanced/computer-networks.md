# Computer Networks

The architecture and engineering of the Internet and the datacenter fabrics beneath modern systems: layering and the end-to-end principle, transport and congestion control, routing at intra- and inter-domain scale, datacenter networking, and the programmable-network (SDN/P4) era. Distributed systems assumes the network; this module opens the box — the diagnostic, the systems specialization, and half the landmark systems papers presume this material.

## Learning objectives

- Explain the Internet architecture — layering, the end-to-end principle, addressing/CIDR, and why IP's "narrow waist" shaped everything above and below it.
- Analyze transport in depth: reliability over an unreliable network, TCP's machinery, congestion control (AIMD, Reno/Cubic, BBR) and its fairness story, and why QUIC moved transport to user space.
- Reason about routing at both scales: link-state and distance-vector intra-domain protocols (OSPF/IS-IS), and BGP with its policy mechanisms, convergence problems, and security pathologies.
- Explain datacenter networking: Clos/leaf–spine topologies, ECMP, incast and DCTCP, and RDMA/kernel-bypass host networking.
- Reason about programmable networks: SDN's control/data-plane separation, OpenFlow, P4, and network verification.
- Measure networks honestly: latency vs. bandwidth vs. loss, bufferbloat, and sound measurement methodology under emulation.

## Prerequisites

- [Operating Systems](../core/operating-systems.md) — the I/O stack and concurrency; sockets-level programming.
- Pairs naturally with [Distributed Systems](../core/distributed-systems.md), before or concurrently.

## Primary resources

- **Kurose & Ross, *Computer Networking: A Top-Down Approach*** — the foundation pass.
- **Peterson & Davie, *Computer Networks: A Systems Approach*** (free online) — the systems-flavored spine.
- **Stanford CS144 (Introduction to Computer Networking)** — the lab sequence (build a TCP implementation); the implementation core of this module.
- **Stanford CS244 / MIT 6.829 (Advanced Topics in Networking)** — the graduate paper-driven pass.

## Seminal papers

- Cerf & Kahn (1974), "A Protocol for Packet Network Intercommunication."
- Saltzer, Reed & Clark (1984), "End-to-End Arguments in System Design" — re-read from the OS module, now in its native habitat.
- Clark (1988), "The Design Philosophy of the DARPA Internet Protocols."
- Jacobson (1988), "Congestion Avoidance and Control" — AIMD; the paper that saved the Internet.
- Stoica et al. (2001), "Chord: A Scalable Peer-to-Peer Lookup Service for Internet Applications."
- McKeown et al. (2008), "OpenFlow: Enabling Innovation in Campus Networks."
- Al-Fares, Loukissas & Vahdat (2008), "A Scalable, Commodity Data Center Network Architecture" — the fat-tree datacenter.
- Alizadeh et al. (2010), "Data Center TCP (DCTCP)."
- Bosshart et al. (2014), "P4: Programming Protocol-Independent Packet Processors."
- Cardwell et al. (2016), "BBR: Congestion-Based Congestion Control."
- Langley et al. (2017), "The QUIC Transport Protocol: Design and Internet-Scale Deployment."

## Assignments

- **Problem sets:** weekly — one congestion-control dynamics problem (AIMD steady state, throughput vs. RTT and loss), one routing trace or BGP policy puzzle, one design question argued from the end-to-end principle.
- **Implementation project:** the CS144-style lab — implement a TCP-like reliable transport over UDP (sliding window, retransmission, congestion control) and validate it under emulated loss and delay (`tc`/netem or Mininet).
- **Measurement study:** compare Reno/Cubic vs. BBR in Mininet across RTTs and buffer sizes; report throughput, fairness, and bufferbloat, and reconcile findings with each algorithm's model.
- **Paper critique:** deep-read BBR or DCTCP via `/paper` — interrogate the fairness claims and how far the evaluation generalizes beyond its setting.

## AI study loop

- `/study computer-networks` for concept passes; trace packet flows by hand before reading the answer.
- `/quiz computer-networks` weekly — congestion-control dynamics and BGP reasoning are the highest-yield drills.
- `/oral-exam computer-networks`; expect "walk this packet from socket to socket" and "what breaks when the link is lossy/long/fat?"

## Mastery checklist

- [ ] Can apply the end-to-end principle to a new design decision and argue both sides.
- [ ] Can walk TCP through a loss episode and derive steady-state throughput from RTT and loss rate.
- [ ] Can explain BGP path selection and construct a policy-induced routing anomaly.
- [ ] Can design a Clos fabric and explain ECMP, incast, and DCTCP's remedy.
- [ ] Can explain what SDN/P4 move between control and data planes, and why.
- [ ] Can connect the topic to current research (programmable data planes, RDMA/host networking, QUIC evolution, network verification, ML for networking).
