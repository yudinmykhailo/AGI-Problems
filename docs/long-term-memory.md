# Long-term memory (Continual Learning)

[← Back to list](../README.md)

**Category:** Technical  
**Problem status:** Unsolved

---
## The essence of the problem

Modern neural networks suffer from “catastrophic forgetting”: when fine-tuned on new data, the network’s weights are overwritten, and previously learned knowledge is destroyed. This makes continuous accumulation of experience - one of the key characteristics of human intelligence - impossible.

A human learns throughout life without losing the skill of riding a bicycle when learning a new language. An AI system with a standard architecture lacks this ability.

---
## Why it is critical

The problem is deeper than just “cannot be fine-tuned.” It means the absence of three fundamentally different types of memory.

**Semantic memory** (facts about the world) in modern LLMs is implemented - but it is static, fixed at the time of training, and not updated.

**Procedural memory** (skills) is also partially present, but degrades when tasks change.

**Episodic memory** (specific events from personal experience - “how it was”) is practically absent. The model does not remember a specific conversation with a specific person a month ago, does not form a personal history. This means the absence of narrative, self-identity, and personalized experience - without which true autonomy is impossible.

---
## Additional context

Biologically, the hippocampus is responsible for memory consolidation: it “replays” events during sleep, gradually transferring important information to the cortex without destroying old connections. This mechanism - Complementary Learning Systems (CLS) - inspires part of the research in continual learning.

---
## How it is being attempted to solve

**Retrieval-Augmented Generation (RAG)** - offloading memory to an external database. The model does not store facts in weights but accesses an external repository when needed. A popular engineering solution, but does not solve the problem of integrating experience.

**Elastic Weight Consolidation (EWC)** - an algorithm that identifies “important” weights and protects them from being overwritten during fine-tuning.

**Progressive Neural Networks** - adding new “columns” for new tasks while preserving old ones.

**Memory-Augmented Neural Networks** - architectures with external differentiable memory (Neural Turing Machine, DNC from DeepMind).

---
## Key persons and works

- **Demis Hassabis** - founder of DeepMind, researcher of memory neurobiology
- **Ilya Sutskever** - work on architectures with long-term memory
- **Geoffrey Hinton** - early work on complementary learning systems

---
## Related problems

- [Embodied intelligence](04-embodied-intelligence.md) - experience requires memory of episodes
- [Autonomous goal setting](12-goal-setting.md) - autonomy requires accumulated experience
- [Meta-learning](06-meta-learning.md) - learning without catastrophic forgetting