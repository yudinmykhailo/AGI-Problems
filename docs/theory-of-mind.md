# Theory of Mind

[← Back to list](../README.md)

**Category:** Cognitive  
**Problem status:** Unsolved

---
## The essence of the problem

Theory of Mind is the ability to understand that other beings have their own beliefs, desires, intentions, and perspectives that differ from your own. It is what allows a person to understand irony, grasp hidden motives, and predict an interlocutor’s actions.

AI sees actions and words. But behind them lie unobservable mental states that determine their meaning. Without a model of these states, communication remains a shallow statistical game.

---
## Why it is critical

**Frame Problem (McCarthy):** AI cannot automatically understand what remains unchanged after an action. If you move a vase - the room is the same, the windows are the same, the table is the same. For a human this is trivial. For a logical system it requires explicitly listing everything that stayed unchanged - an infinite task.

The second dimension is **collective norms**. Theory of Mind is needed not only to understand a specific interlocutor but also to grasp unwritten social rules that no one has explicitly explained: what is considered rude, what is polite, what is appropriate in a given context and culture.

An AI lacking these abilities will regularly “miss” in social situations, even with formally correct answers.

---
## Additional context

The psychological test for Theory of Mind is the Sally-Ann task: a child under 4 years old does not understand that another person can have a false belief. After age 4 - they understand. Modern LLMs show contradictory results on similar tests: they perform well on the canonical formulation but break down on paraphrases.

---
## How it is being attempted to solve

**Training on scenarios with a mental model** - datasets like ToMi, where models are explicitly taught to reason about agent states.

**Contextual emotion analysis** - integrating emotional signals into the architecture (Affective Computing, Rosalind Picard).

**Embedding ethical and social norms** (RLHF, Constitutional AI) - attempting to transfer through training what cannot be deduced from text.

**Simulation of social environments** - training agents in multi-agent environments where they need to model the behavior of other agents.

---
## Key persons and works

- **Rosalind Picard** — Affective Computing, MIT Media Lab.
  [Affective Computing (book)](https://mitpress.mit.edu/9780262661157/affective-computing/)
- **John McCarthy** — formalization of the Frame Problem.
  [Some Philosophical Problems from the Standpoint of Artificial Intelligence](https://www.sciencedirect.com/science/article/pii/B9780934613033500276)
- **Annette Karmiloff-Smith** — neurodevelopmental foundations of Theory of Mind.
  [Beyond Modularity: A Developmental Perspective on Cognitive Science](https://mitpress.mit.edu/9780262611312/beyond-modularity/)
- **Anthropic team** — Constitutional AI and social alignment.
  [Constitutional AI: Harmlessness from AI Feedback](https://arxiv.org/abs/2212.08073)

---
## Related problems

- [Common sense](common-sense.md) - social norms as part of common sense
- [Causal reasoning](causal-reasoning.md) - reasoning about intentions as causes of actions
- [Consciousness](consciousness.md) - connection between self-awareness and understanding other minds