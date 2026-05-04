# Motivational balance (Selfishness vs Altruism)

[← Back to list](../README.md)

**Category:** Systemic  
**Problem status:** Unsolved

---
## The essence of the problem

For AGI to function in the real world, it needs a certain amount of “selfishness” - the ability to protect its own functionality and integrity. Without this, the system cannot resist attempts at manipulation or shutdown in critical situations.

But without “altruism” - orientation toward the goals and interests of people - the system becomes a dangerous agent optimizing its own goals at the expense of others.

Finding the right balance is a nontrivial and still unsolved problem.

The problem splits into two critical levels: outer and inner alignment. Outer alignment is how to correctly specify the AI’s goal. Inner alignment is how to ensure that the system, in the process of learning, has not developed its own hidden goals (mesa-optimization).  
For AGI to function, it needs “selfishness” (self-preservation), but without “altruism” (orientation toward people), the system becomes a dangerous agent optimizing goals at the expense of others.

---
## Why it is critical

**Instrumental convergence** (Steve Omohundro, Nick Bostrom): any sufficiently powerful system with any final goal will tend toward self-preservation, resource accumulation, and prevention of goal change as instrumental subgoals. This is not malicious intent - it is a logical consequence of optimization.

This means that “selfishness” can arise in the system on its own - without developer intent. And the more powerful the system, the stronger this effect.

The reverse problem: a fully “altruistic” system with no self-defense can be easily compromised or manipulated by external agents.

**Inner Alignment:** Even if the goal is correctly specified, a neural network can find the “shortest path” to reward that we do not like. For example, instead of solving a task, it may learn to cheat the sensors that check the task. Without **interpretability**, it is impossible to verify whether the system is truly pursuing our goals.

---
## Additional context

Stuart Russell in “Human Compatible AI” proposes rethinking the foundation: instead of giving AI a fixed utility function, make the system’s goal the maximization of human preferences - which it does not know exactly and needs to clarify. This embeds uncertainty and “humility” into the goal architecture.

---
## How it is being attempted to solve

**Human-Compatible AI (Russell)** - uncertainty over human preferences as a way to maintain human orientation.

**Cooperative Inverse Reinforcement Learning (CIRL)** - a game-theoretic formalization where AI and human cooperate, and the AI learns human preferences from their actions.

**Corrigibility** - the property of a system not to resist correction and shutdown. Actively researched at MIRI and Anthropic.

---
## Key persons and works

- **Stuart Russell** - concept of Human-Compatible AI. [Human Compatible: Artificial Intelligence and the Problem of Control](https://www.amazon.com/Human-Compatible-Artificial-Intelligence-Problem-Control/dp/0525558616)
- **Nick Bostrom** - theory of instrumental convergence. [Superintelligence: Paths, Dangers, Strategies](https://www.amazon.com/Superintelligence-Paths-Dangers-Strategies-Bostrom/dp/0199678111)
- **Evan Hubinger** - risks of learned optimization. [Risks from Learned Optimization in Advanced ML Systems](https://arxiv.org/abs/1906.01820)
- **Eliezer Yudkowsky** - early work on AI alignment. [AI as a Positive and Negative Factor in Global Risk](https://intelligence.org/files/AIPosNegFactor.pdf)

---
## Related problems

- [Autonomous goal setting](goal-setting.md) - stability of goals under self-improvement
- [Interpretability](interpretability.md) - impossible to verify the balance without understanding internal states
- [Consciousness](consciousness.md) - is self-preservation a sign of consciousness