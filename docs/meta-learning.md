# Meta-learning (Learning to Learn)

[← Back to list](../README.md)

**Category:** Technical / Cognitive  
**Problem status:** Actively researched

---
## The essence of the problem

A four-year-old child sees an unfamiliar animal once - and remembers it. A modern neural network requires thousands or millions of examples to reliably recognize a new class of objects.

This is not just a question of efficiency. It points to a fundamental difference in how the learning algorithm itself is structured. Humans learn to learn - they use accumulated experience to master new skills faster. Current AI systems lack this ability.

---
## Why it is critical

It is important to distinguish meta-learning from related concepts.

**Transfer learning** - transferring already learned features to a new task. This is a partial solution, but not meta-learning: the model does not improve its learning algorithm, it uses old knowledge as initialization.

**Meta-learning** - when a system learns to adapt quickly to new tasks because it has improved its internal learning algorithm based on experience from previous tasks.

Without meta-learning, AGI will require huge amounts of data and computation every time it encounters a new domain. This makes it qualitatively less intelligent than a child.

---
## Additional context

Josh Tenenbaum (MIT) shows that children use rich Bayesian prior models of the world to generalize from one or a few examples. They do not just “memorize” - they build hypotheses about the hidden structure of categories.

Yann LeCun argues that the next frontier after self-supervised learning should be architectures that explicitly optimize the speed and quality of learning, not just prediction quality.

---
## How it is being attempted to solve

**MAML (Model-Agnostic Meta-Learning)** - Chelsea Finn. An algorithm that trains a weight initialization such that a few steps of gradient descent yield good quality on a new task.

**Few-Shot Learning** - learning from a small number of examples using metric spaces (Prototypical Networks, Matching Networks).

**Neural Processes** - a family of architectures that learn to build probabilistic models of functions from a small number of points.

**In-context learning (LLM)** - GPT-4 and similar models demonstrate impressive few-shot behavior directly in context, without updating weights. Whether this is true meta-learning is a debated question.

---
## Key persons and works

- **Chelsea Finn** — MAML, pioneer of modern meta-learning.
  [Model-Agnostic Meta-Learning for Fast Adaptation of Deep Networks](https://arxiv.org/abs/1703.03400)
- **Yann LeCun** — theorist of sample-efficient learning.
  [A Path Towards Autonomous Machine Intelligence](https://openreview.net/pdf?id=BZ5aUm_I9_H)
- **Josh Tenenbaum** — cognitive foundations of meta-learning.
  [How to Grow a Mind: Statistics, Structure, and Abstraction](https://www.science.org/doi/10.1126/science.1192788)
- **Oriol Vinyals** — Matching Networks, few-shot learning at DeepMind.
  [Matching Networks for One Shot Learning](https://arxiv.org/abs/1606.04080)

---
## Related problems

- [Long-term memory](long-term-memory.md) - using past experience for fast learning
- [Embodied intelligence](embodied-intelligence.md) - learning through interaction
- [Common sense](common-sense.md) - prior knowledge accelerates learning