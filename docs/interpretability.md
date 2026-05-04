# Interpretability (Black box)

[← Back to list](../README.md)

**Category:** Philosophical  
**Problem status:** Actively researched

---
## The essence of the problem

Modern neural networks make decisions in ways that their creators cannot understand or explain. We can observe the inputs and output predictions, but what happens inside - billions of numerical operations - remains opaque.

This is not just an academic problem. It is a practical blocker for any serious application of AI.

---
## Why it is critical

Interpretability is a systemic blocker: without it, many other problems in this repository become unsolvable.

**Value alignment** cannot be verified if we cannot look inside and ensure that the system is indeed pursuing the goals we set - rather than optimizing superficial proxies.

**Error diagnosis** is impossible without understanding their causes. We may notice that the model makes mistakes in certain cases, but we cannot understand why - and therefore cannot fix it.

**Trust in critical domains** - medicine, law, security - requires explainability. “The neural network decided so” is not sufficient justification for denying a loan or making a diagnosis.

---
## Additional context

**Mechanistic Interpretability** - a direction actively developed by Anthropic. The goal is to understand which algorithms are implemented in specific neural networks at the level of individual neurons and circuits. The Anthropic team discovered that many neurons encode multiple unrelated concepts simultaneously (superposition), making the task fundamentally difficult.

Chris Olah in a series of “Circuits” works showed that in visual models, specific detectors of curves, eyes, textures can be identified - and traced how they combine. This is a proof of principle that interpretability is attainable - though scaling to large models remains an open problem.

---
## How it is being attempted to solve

**LIME and SHAP** - post-hoc explanation methods: for a given prediction, they show which input features were most important. Useful in practice but do not provide understanding of mechanisms.

**Attention visualization** - visualization of attention weights in transformers. Intuitively understandable but poorly correlated with the actual causes of predictions.

**Mechanistic Interpretability** (Olah, Anthropic) - understanding the specific computational circuits within the network. Labor-intensive but provides genuine understanding.

**Probing classifiers** - training separate classifiers on intermediate activations to check which concepts are encoded in different layers.

**Activation Patching** - a method for determining the causal role of specific activations in a prediction.

---
	## Key persons and works

- **Chris Olah** - Circuits, founder of Mechanistic Interpretability
- **Anthropic Interpretability Team** - scaling MI to large models
- **Scott Lundberg** - SHAP values
- **Zack Cohen** - theoretical foundations of interpretability

---
## Related problems

- [Motivational balance](11-motivational-balance.md) - verification of embedded values
- [Autonomous goal setting](12-goal-setting.md) - verification of the system’s goals
- [Consciousness](14-consciousness.md) - interpretability as a necessary condition for detecting consciousness