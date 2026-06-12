# Reinforcement Learning

Sequential decision-making under uncertainty: the MDP formalism and dynamic programming, the exploration–exploitation problem and its regret theory, value-based and policy-gradient deep RL, model-based and offline RL, and the alignment applications (RLHF) that have made RL central to modern AI. The discipline is in reasoning about sample complexity, stability, and what an agent is actually optimizing.

## Learning objectives

- Formalize problems as MDPs/POMDPs and solve them with value/policy iteration; state and use the Bellman optimality equations and contraction arguments.
- Analyze exploration via regret: derive bounds for UCB and Thompson sampling in bandits and explain how they extend to RL.
- Derive and implement value-based (Q-learning, DQN) and policy-gradient (REINFORCE, actor-critic, PPO/TRPO) methods, and explain their stability failure modes.
- Reason about model-based RL, offline RL, and the deadly triad (function approximation + bootstrapping + off-policy).
- Explain RLHF/preference optimization and the reward-modeling and reward-hacking issues it raises.

## Prerequisites

- [Machine Learning Foundations](../core/machine-learning.md) — function approximation, SGD.
- [Mathematics for CS Research](../core/math-for-cs.md) — probability, optimization; dynamic programming.
- Note: core ML's RL unit (Sutton & Barto ch. 1–10, DQN) is the on-ramp; this module assumes it and owns the depth — including the RLHF mechanism the NLP module uses.

## Primary resources

- **Sutton & Barto, *Reinforcement Learning: An Introduction*** (free online) — the canonical text.
- **Lattimore & Szepesvári, *Bandit Algorithms*** (free online) — for the regret-theory unit.
- **UC Berkeley CS285 (Deep RL)** and **DeepMind/UCL RL Lectures (Silver)** — lectures and assignments.
- **Agarwal, Jiang, Kakade & Sun, *Reinforcement Learning: Theory and Algorithms*** (free online) — the theory track.
- **Spinning Up in Deep RL** (OpenAI) — implementation reference.

## Seminal papers

- Watkins & Dayan (1992), "Q-learning."
- Sutton, McAllester, Singh & Mansour (2000), "Policy Gradient Methods for Reinforcement Learning with Function Approximation."
- Mnih et al. (2015), "Human-Level Control through Deep Reinforcement Learning" (DQN).
- Schulman et al. (2017), "Proximal Policy Optimization Algorithms."
- Silver et al. (2017), "Mastering the Game of Go without Human Knowledge" (AlphaGo Zero).
- Haarnoja et al. (2018), "Soft Actor-Critic" — maximum-entropy RL.
- Auer, Cesa-Bianchi & Fischer (2002), "Finite-Time Analysis of the Multiarmed Bandit Problem" (UCB).
- Levine et al. (2020), "Offline Reinforcement Learning: Tutorial, Review, and Perspectives."
- Christiano et al. (2017), "Deep Reinforcement Learning from Human Preferences" (RLHF).

## Assignments

- **Problem sets:** weekly — one Bellman/contraction proof, one regret-bound derivation, one policy-gradient derivation.
- **Implementation project:** implement DQN and PPO from scratch on standard benchmarks; reproduce a learning curve and document the engineering choices that decide success or collapse.
- **Exploration study:** implement UCB and Thompson sampling on a bandit, empirically measure regret, and compare to the theoretical bound.
- **Paper critique:** deep-read the RLHF paper via `/paper` — interrogate the reward-model assumption and where reward hacking enters.

## AI study loop

- `/study reinforcement-learning` for concept passes; derive the gradient/bound before seeing it.
- `/quiz reinforcement-learning` weekly — Bellman reasoning and regret bounds are the highest-yield drills.
- `/oral-exam reinforcement-learning`; expect "what is this agent actually maximizing, and why is training unstable?"

## Mastery checklist

- [ ] Can prove convergence of value iteration via the contraction property.
- [ ] Can derive UCB or a Thompson-sampling regret bound.
- [ ] Can derive the policy-gradient theorem and implement an actor-critic.
- [ ] Can explain the deadly triad and DQN's stabilization tricks.
- [ ] Can explain RLHF end-to-end and name concrete reward-hacking risks.
- [ ] Can connect the topic to current research (RLHF/RLAIF, offline RL, RL for reasoning in LLMs, world models).
