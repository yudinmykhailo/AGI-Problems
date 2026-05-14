# Problems on the Path to AGI

> A structured reference on fundamental barriers to Artificial General
> Intelligence - from engineering constraints to philosophical unknowns.

This repository describes **19 unsolved problems** that must be addressed before AGI becomes possible. Each problem has its own page with: what it is, why it is a *fundamental* barrier (not just an engineering challenge), current research approaches, key figures with links to their work, and connections to related problems.

---
## Categories

| Category         | Problems |
| ---------------- | :------: |
| 🔧 Technical     |    5     |
| 🧩 Cognitive     |    6     |
| 🔗 Systemic      |    6     |
| 🔮 Philosophical |    2     |

---
## 🔧 Technical

Engineering and architectural limitations of current AI systems.

| Problem | Description                                                                                                                      | Status |
|---------|-------------|--------|
| [Emotions as an Evaluation System](docs/emotions-as-evaluation.md) | No sense of importance or danger - cannot intuitively filter wrong decisions. Goodhart's Law makes proxy metrics unreliable.     | 🔴 Unsolved |
| [Energy Efficiency](docs/energy-efficiency.md) | Massive energy costs vs. the brain's 20W. Exponential compute for linear capability gains.                                       | 🟡 Partial |
| [Long-Term Memory](docs/long-term-memory.md) | Catastrophic forgetting when learning new things. No episodic memory - no personal history.                                      | 🔴 Unsolved |
| [Embodied Intelligence](docs/embodied-intelligence.md) | No understanding of the physical world. Symbol Grounding Problem: symbols without sensorimotor experience have no real referent. | 🔴 Unsolved |
| [Robustness](docs/robustness.md) | Catastrophic failure under minimal deviation from training distribution. A 1% change can break the system.                       | 🟡 Active |

---
## 🧩 Cognitive

Fundamental gaps between machine and human thinking.

| Problem | Description                                                                                                              | Status |
|---------|-------------|--------|
| [Meta-Learning](docs/meta-learning.md) | Humans learn from 2–3 examples; AI needs millions. The limitation is in the learning algorithm itself.                   | 🟡 Active |
| [Theory of Mind](docs/theory-of-mind.md) | Sees actions but doesn't understand motives or intentions. Cannot grasp collective unwritten norms.                      | 🔴 Unsolved |
| [Causal Reasoning](docs/causal-reasoning.md) | Relies on statistics without understanding "why." Missing abductive reasoning - forming hypotheses from incomplete data. | 🟡 Active |
| [Compositional Generalization](docs/compositional-generalization.md) | Cannot reliably combine familiar concepts in new configurations. Matches patterns rather than composes rules.            | 🔴 Unsolved |
| [Common Sense](docs/common-sense.md) | No tacit foundation of world knowledge. Cannot be fixed by more data - common sense is never written down.               | 🔴 Unsolved |
| [Hierarchical Planning](docs/hierarchical-planning.md) | Cannot hold and pursue goals over long time horizons. Loses the objective as planning depth increases.                   | 🔴 Unsolved |

---
## 🔗 Systemic

Problems in designing AGI motivation, goals, and multi-agent dynamics.

| Problem | Description | Status |
|---------|-------------|--------|
| [Motivational Balance](docs/motivational-balance.md) | Without "selfishness" AI can't protect itself; without "altruism" it becomes dangerous. Instrumental convergence makes self-preservation emerge on its own. | 🔴 Unsolved |
| [Autonomous Goal-Setting](docs/goal-setting.md) | AI is a passive tool. Without intrinsic motivation there is no autonomy. Goals may not survive self-improvement. | 🔴 Unsolved |
| [Value Learning](docs/value-learning.md) | Human values are implicit, contradictory, and change over time. No complete specification exists to learn from. | 🔴 Unsolved |
| [Recursive Self-Improvement](docs/recursive-self-improvement.md) | A system improving its own architecture faster than humans can audit it. Goals may not survive the rewrite. | 🟠 Theoretical |
| [Social Intelligence & Cooperation](docs/multi-agent-cooperation.md) | Multi-agent environments are non-stationary. Even well-aligned agents can produce collectively bad emergent outcomes. | 🟡 Active |
| [Formal Verification](docs/formal-verification.md) | We can test but not *prove* safe behavior under all conditions. Verification methods do not scale to large neural networks. | 🔴 Unsolved |

---
## 🔮 Philosophical

Conceptual barriers that cannot be resolved by engineering alone.

| Problem                                      | Description                                                                                                          | Status    |
| -------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | --------- |
| [Interpretability](docs/interpretability.md) | We cannot understand why a system makes a decision. Blocks value alignment verification, error diagnosis, and trust. | 🟡 Active |
| [Consciousness](docs/consciousness.md)       | Will AGI truly understand, or simulate understanding? The Hard Problem makes any test philosophically vulnerable.    | 🔴 Open   |

---
## Status legend

| Badge          | Meaning                                              |
| -------------- | ---------------------------------------------------- |
| 🔴 Unsolved    | No convincing solution or clear path to one          |
| 🟠 Theoretical | Formal frameworks exist; no practical implementation |
| 🟡 Active      | Actively researched; partial results exist           |
| 🔴 Open        | Philosophical - may not have an empirical solution   |

---
## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to propose new problems or improve existing pages.