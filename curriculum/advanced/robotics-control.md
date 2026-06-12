# Robotics and Control

Getting physical systems to act intelligently in the world: the dynamics and control theory that guarantee stability, state estimation under noise, motion planning, optimal and model-predictive control, and the learning-based methods that now augment (but rarely replace) classical guarantees. The discipline lives at the seam between provable control and data-driven policies.

## Learning objectives

- Model dynamical systems (state-space, rigid-body dynamics) and analyze stability via Lyapunov theory and linear-systems tools.
- Design feedback controllers (PID, LQR, LQG) and reason about controllability, observability, and robustness.
- Perform state estimation under uncertainty with the Kalman filter family and particle filters; explain the estimation/control duality.
- Formulate and solve motion-planning problems (sampling-based planners, trajectory optimization) and model-predictive control.
- Situate learning-based control (imitation learning, sim-to-real, RL for control) against classical guarantees, and reason about safety.

## Prerequisites

- [Mathematics for CS Research](../core/math-for-cs.md) — linear algebra, ODEs, optimization, probability.
- Helpful: [Reinforcement Learning](reinforcement-learning.md) for the learning-based control unit.

## Primary resources

- **Tedrake, *Underactuated Robotics*** (free online, MIT 6.832) — dynamics, LQR, trajectory optimization; the spine.
- **Åström & Murray, *Feedback Systems*** (free online) — control fundamentals.
- **Thrun, Burgard & Fox, *Probabilistic Robotics*** — estimation, SLAM, the Bayes-filter view.
- **LaValle, *Planning Algorithms*** (free online) — motion planning.
- **Boyd & Vandenberghe, *Convex Optimization*** (free online) — the optimization backbone for MPC.

## Seminal papers

- Kalman (1960), "A New Approach to Linear Filtering and Prediction Problems."
- LaValle & Kuffner (2001), "Randomized Kinematic Planning" / RRT.
- Kavraki et al. (1996), "Probabilistic Roadmaps for Path Planning in High-Dimensional Configuration Spaces."
- Todorov, Erez & Tassa (2012), "MuJoCo: A Physics Engine for Model-Based Control."
- Levine et al. (2016), "End-to-End Training of Deep Visuomotor Policies."
- Pomerleau (1989), "ALVINN" / Ross, Gordon & Bagnell (2011), "DAgger" — imitation learning.
- Mayne et al. (2000), "Constrained Model Predictive Control: Stability and Optimality."
- Tobin et al. (2017), "Domain Randomization for Transferring Deep Neural Networks from Simulation to the Real World."

## Assignments

- **Problem sets:** weekly — one stability/Lyapunov proof, one estimator derivation (Kalman), one planning or LQR design problem.
- **Implementation project:** implement LQR and an EKF for a simulated system (cart-pole or quadrotor); then add a learned or MPC controller and compare stability, robustness, and sample efficiency.
- **Planning project:** implement an RRT* or trajectory-optimization planner and benchmark it against constraints/obstacles, reporting path quality and runtime.
- **Paper critique:** deep-read the visuomotor-policy or domain-randomization paper via `/paper` — interrogate the sim-to-real gap and what safety guarantee (if any) survives.

## AI study loop

- `/study robotics-control` for concept passes; derive the controller/estimator before seeing it.
- `/quiz robotics-control` weekly — Lyapunov stability and Kalman filtering are the highest-yield drills.
- `/oral-exam robotics-control`; expect "prove this controller is stable" and "what happens when your model is wrong?"

## Mastery checklist

- [ ] Can analyze stability via Lyapunov functions and check controllability/observability.
- [ ] Can derive and implement an LQR controller and a Kalman/EKF estimator.
- [ ] Can formulate and solve a trajectory-optimization or MPC problem.
- [ ] Can implement a sampling-based motion planner and reason about completeness.
- [ ] Can compare learned vs classical control and articulate the safety trade-offs.
- [ ] Can connect the topic to current research (learned dynamics/world models, safe RL, robot foundation models, sim-to-real).
