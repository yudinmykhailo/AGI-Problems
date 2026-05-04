# Robustness (Resilience to unforeseen conditions)

[← Back to list](../README.md)

**Category:** Technical  
**Problem status:** Actively researched

---
## The essence of the problem

Modern AI systems catastrophically break down at minimal deviations from the conditions they were trained on. A small change in lighting in a photo, a few pixels of noise, an unusual formulation of a question - and the system that shows expert-level results under standard conditions starts making gross errors.

A human under the same conditions does not notice the difference.

---
## Why it is critical

This problem is separate from compositional generalization. That one deals with novel concepts. Here it is about fragility to variations of already familiar situations.

**Adversarial examples** (Goodfellow, 2014): adding specially crafted noise, invisible to humans, changes a confident classification of “cat” into a confident classification of “ostrich.” The model responds not to the object but to statistical patterns in pixels.

For any AGI operating in the real world, this is a critical barrier. Medical diagnostics, car control, industrial systems - all face conditions not present in the training set. Without robustness, AGI cannot be trusted with any decision having real consequences.

**Distribution shift** - a broader version of the same problem: a model trained on data from one period or source degrades on data from another.

---
## Additional context

The deep cause of fragility is that neural networks learn to use non-representative, “surface” features (spurious correlations). A model for recognizing cows may learn to recognize the green meadow in the background because in the training set cows were always photographed in nature. On an image of a cow indoors, it will err.

---
## How it is being attempted to solve

**Adversarial training** - including adversarial examples in the training set. Improves resistance to attacks but reduces accuracy on clean data.

**Certified robustness** - mathematical guarantees that the prediction will not change within an ε-neighborhood of the input. Currently works only for small networks.

**Data augmentation** - aggressive expansion of the training set with variations to reduce overfitting to a specific distribution.

**Causal representation learning** - learning causal rather than correlational features. Theoretically should eliminate spurious correlations.

---
## Key persons and works

- **Ian Goodfellow** - discovery of adversarial examples.
  [Explaining and Harnessing Adversarial Examples](https://arxiv.org/abs/1412.6572)
- **Nicholas Carlini** - attacks, defenses, and robustness metrics.
  [Evaluating the Robustness of Neural Networks](https://arxiv.org/abs/1608.04644)
- **Bernhard Schölkopf** - causal approaches to robustness.
  [Toward Causal Representation Learning](https://arxiv.org/abs/2102.11107)
---
## Related problems

- [Causal reasoning](causal-reasoning.md) - causal features are more robust than correlational ones
- [Common sense](common-sense.md) - intuitive plausibility checking of results
- [Interpretability](interpretability.md) - understanding what features the model relies on