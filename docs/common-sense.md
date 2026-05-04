# Common sense and implicit world model

[← Back to list](../README.md)

**Category:** Cognitive  
**Problem status:** Unsolved

---
## The essence of the problem

A huge body of knowledge that every person possesses is never written down explicitly - because it is “obvious.” A glass dropped from a height will break. The dead do not come back to life. A person cannot walk through a wall. Fire burns.

AI trained on text lacks this foundation - because no one writes articles about the dead not coming back to life. It is nowhere formulated. It is just known.

---
## Why it is critical

The common sense problem is fundamentally unsolvable by scaling data. Unlike most other AI problems where “more data” at least partially helps, here that path is closed: you can only add what is written. And what is obvious is not written.

This means that systems trained only on text will systematically “hallucinate” in edge cases requiring physical intuition or basic life experience - not because they are not smart enough, but because they structurally lack the required type of knowledge.

---
## Additional context

**Project Cyc (Douglas Lenat, 1984–2017)** - an attempt to manually encode common sense: in 33 years about 25 million rules were written. That is roughly as much as a 4-year-old child knows “just like that.” The project showed the scale of the problem and the futility of the manual approach.

**ConceptNet** - an open knowledge base of common sense. A useful resource, but it covers only the surface of what is needed.

Yann LeCun points out that the solution likely lies in learning through physical interaction with the world - what children do in the first years of life before they learn to speak.

---
## How it is being attempted to solve

**Physical simulators** - training agents in virtual worlds where they gain experience with objects (falling, collision, deformation).

**World Models (LeCun)** - learning an internal predictive model of the world’s physics.

**ConceptNet + neural networks** - hybrid approaches where the knowledge base is used as an auxiliary resource for neural network models.

**Multimodal learning** - integrating video, physical simulations, and text to form a more complete world model.

---
## Key figures

- **Douglas Lenat** - founder of the Cyc project
- **Yann LeCun** - critic of language models, proponent of world models
- **Gary Marcus** - systematic critique of LLM limitations
- **Ernest Davis** - formalization of common sense and physical knowledge

---
## Related problems

- [Embodied intelligence](04-embodied-intelligence.md) - physical experience as a source of common sense
- [Robustness](05-robustness.md) - common sense as a mechanism for checking plausibility
- [Compositional generalization](09-compositional-generalization.md) - applying rules to new situations