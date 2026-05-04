# Compositional generalization

[← Back to list](../README.md)

**Category:** Cognitive  
**Problem status:** Unsolved

---
## The essence of the problem

A person who knows the words “red,” “cube,” and “quickly” effortlessly understands “quickly moving red cube,” even having never encountered that exact description. This is called systematicity of thought: the meaning of the whole is built from the meaning of the parts according to rules.

Modern neural networks struggle with this. They work well on combinations encountered in the training set, but break on new combinations of known elements.

---
## Why it is critical

Noam Chomsky described the principle of linguistic productivity: from a finite vocabulary and a finite set of rules, one can build an infinite number of meaningful sentences. The human mind follows this principle not only in language but also in thinking in general.

Transformers do not follow this principle. They approximate a function that describes the training data well, but does not necessarily generalize correctly. This means that when confronted with non-standard combinations - of which there are countless in the real world - the system will regularly fail.

This makes AGI based on current architectures unreliable in an open world: any new configuration of familiar objects is a potential failure point.

---
## Additional context

**SCAN benchmark (Brendan Lake)** - a standard test for compositional generalization. Models are trained on commands like “jump” → “jump” and “twice” → “twice”, then tested on “jump twice”. Standard neural networks perform much worse than humans.

Gary Marcus systematically criticizes deep learning precisely for its inability to generalize systematically and proposes hybrid neuro-symbolic architectures as a solution.

---
## How it is being attempted to solve

**Neuro-symbolic hybrids** - combining neural networks (for perception and generalization) with symbolic systems (for applying rules). NS-CL, DreamCoder.

**Relational Networks** - architectures with explicit modeling of relations between objects.

**Equivariant Neural Networks** - networks explicitly invariant to certain transformations.

**Program synthesis** - learning to generate programs, not numerical answers. Programs are compositional by definition.

---
## Key persons and works

- **Gary Marcus** - critique of deep learning, neuro-symbolic approaches
- **Brendan Lake** - SCAN benchmark, cognitive foundations of generalization
- **Daphne Koller** - probabilistic graphical models and generalization
- **Josh Tenenbaum** - program synthesis, DreamCoder

---
## Related problems

- [Causal reasoning](08-causal-reasoning.md) - causal reasoning requires compositionality
- [Common sense](10-common-sense.md) - applying rules to new situations
- [Meta-learning](06-meta-learning.md) - fast generalization from few examples