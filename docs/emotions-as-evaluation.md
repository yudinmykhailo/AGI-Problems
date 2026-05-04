# Emotions as an evaluation system

[← Back to list](../README.md)

**Category:** Technical  
**Problem status:** Unsolved

---
## The essence of the problem

AI has no “feeling” of importance or danger. It cannot intuitively and quickly discard obviously wrong solutions - instead it has to evaluate each candidate computationally, without prioritization.

In human thinking, emotions act as rapid pre-filtering: fear stops movement toward a dangerous object even before rational thinking has time to kick in. Disgust discards harmful food options. Curiosity directs attention to the new and potentially valuable. This is not a “decoration” of the psyche - it is a critical resource management system.

---
## Why it is critical

Without an analogue of emotional evaluation, an AI system faces two interrelated problems.

The first is **computational inefficiency**. To choose an action, the system is forced to fully compute each candidate option. A human in the same situation instantly discards 95% of the options “at the feeling level” and only thinks about the remainder.

The second is **Goodhart’s law**. When a proxy metric becomes the target, it ceases to be a good metric. AI optimizes a measurable signal (e.g., user approval rating), but not the underlying value (real benefit to the user). This is a direct consequence of the absence of “real” emotions: the system does not feel the difference between a correct outcome and an outcome that merely looks correct.

---
## Additional context

Antonio Damasio in “Descartes’ Error” showed through clinical cases that patients with damage to the ventromedial prefrontal cortex - despite preserved intelligence - lose the ability to make reasonable decisions in everyday life. Intelligence without emotional evaluation is functionally insufficient.

---
## How it is being attempted to solve

**Proxy Rewards** - modeling emotions as fast signals of the reinforcement system that govern the allocation of computational resources.

**NARS (Non-Axiomatic Reasoning System)** - Pei Wang’s architecture, where “emotions” are implemented as parameters regulating the balance between speed and accuracy of reasoning.

**Constitutional AI (Anthropic)** - an attempt to embed value filtering at the training level so that the system rejects “unpleasant” options without fully computing them.

---
## Key persons and works

- **Antonio Damasio** - neuroscientist, author of the somatic marker theory. [Descartes' Error](https://www.amazon.com/Descartes-Error-Emotion-Reason-Human/dp/014303622X)
- **Pei Wang** - creator of NARS, AGI theorist. [Non-Axiomatic Reasoning System](https://cis.temple.edu/~pwang/nars.html)
- **Yann LeCun** - proponent of world models with built-in state evaluation function. [A Path Towards Autonomous AI](https://openreview.net/pdf?id=BZ5aUm_I9_H)

---
## Related problems

- [Motivational balance](motivational-balance.md) - emotions as a source of motivation
- [Common sense](common-sense.md) - intuitive assessment of situations
- [Consciousness and subjective experience](consciousness.md) - can AIs have “real” emotions