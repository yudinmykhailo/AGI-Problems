# Common sense and implicit world model

[← Back to list](../README.md)

**Category:** Cognitive  
**Problem status:** Unsolved

---
## The essence of the problem

A huge body of knowledge that every person possesses is never written down explicitly - because it is “obvious.” A glass dropped from a height will break. The dead do not come back to life. A person cannot walk through a wall. Fire burns.

AI trained on text lacks this foundation - because no one writes articles about the dead not coming back to life. It is nowhere formulated. It is just known.

This gap has a name: the **frame problem** - originally posed in AI in 1969 (McCarthy & Hayes). When a situation changes, which facts remain true and which do not? Humans solve this effortlessly. For a formal system, every trivial action (moving a cup) requires explicitly specifying everything that _did not_ change. The combinatorial explosion is immediate.

---
## Why it is critical

The common sense problem is fundamentally unsolvable by scaling data. Unlike most other AI problems where “more data” at least partially helps, here that path is closed: you can only add what is written. And what is obvious is not written.

**Failure example.** GPT-4, asked "I left my cup of coffee on the roof of my car and drove away - where is the coffee now?", produces a correct answer. But structurally similar questions with slight physical variation reveal the brittleness: the model is pattern-matching against surface similarity to seen text, not simulating physics. The same class of model confidently states that a wooden ball placed inside a rubber ball will float - because it "knows" wood floats, without modeling containment. _(Studies: Bisk et al., PIQA benchmark, 2019; Storks et al., 2021)_

This means that systems trained only on text will systematically “hallucinate” in edge cases requiring physical intuition or basic life experience - not because they are not smart enough, but because they structurally lack the required type of knowledge.

---
## Additional context

**Project Cyc (Douglas Lenat, 1984–2017)** - an attempt to manually encode common sense: in 33 years about 25 million rules were written. That is roughly as much as a 4-year-old child knows “just like that.” The project showed the scale of the problem and the futility of the manual approach.

**ConceptNet** - an open knowledge base of common sense. A useful resource, but it covers only the surface of what is needed.

Yann LeCun points out that the solution likely lies in learning through physical interaction with the world - what children do in the first years of life before they learn to speak.

---
## Why scaling does not solve this

This deserves its own elaboration beyond the one-sentence mention above. Three structural reasons:
- **No signal in text.** Text describes events, not the physics underneath them. "She dropped the vase" contains zero information about trajectory, mass, or fragility - a reader reconstructs that from embodied memory, not from the sentence.
- **Distribution of the obvious.** Edge cases that violate common sense are _underrepresented_ in training data precisely because they are surprising - humans do not narrate what does not happen.
- **Systematic gaps vs. random gaps.** More data reduces random gaps. But the absence of embodied knowledge is _systematic_ - it is structurally absent from the text modality, not just underrepresented.

---
## How it is being attempted to solve

**Physical simulators** - training agents in virtual worlds where they gain experience with objects (falling, collision, deformation).

**World Models (LeCun)** - learning an internal predictive model of the world’s physics.

**ConceptNet + neural networks** - hybrid approaches where the knowledge base is used as an auxiliary resource for neural network models.

**Multimodal learning** - integrating video, physical simulations, and text to form a more complete world model.

**Intuitive physics benchmarks as training signal** - using structured test sets (PIQA, PhysicalIQA, PTR) not just for evaluation but as explicit training objectives to force physical plausibility.

**Foundation World Models** - recent direction (2023-2024) pushing toward large pretrained models of environment dynamics, analogous to LLMs but trained on video and sensor data rather than text (Genie, DIAMOND, DreamerV3).
 
---
### Benchmarks

- [PIQA](https://arxiv.org/abs/1911.11641) (Bisk et al., 2019) - physical intuition: "how do you separate egg whites?" - tests procedural physical knowledge
- [HellaSwag](https://arxiv.org/abs/1905.07830) (Zellers et al., 2019) - plausible next-event prediction requiring world knowledge
- [PhysicalIQA / PTR](https://arxiv.org/abs/2109.08309) - compositional physical reasoning
- [WinoGrande](https://arxiv.org/abs/1907.10641) - commonsense pronoun resolution at scale

Note: current LLMs score surprisingly high on many of these benchmarks - which has _not_ resolved the debate, but shifted it toward whether benchmark saturation reflects genuine understanding or sophisticated pattern matching.

---
## Key persons and works

- **Doug Lenat** - founder of the Cyc project, 33 years of common-sense encoding.
  [CYC: A Large-Scale Investment in Knowledge Infrastructure](https://dl.acm.org/doi/10.1145/219717.219745)
- **Yann LeCun** - critic of language models, world models advocate.
  [A Path Towards Autonomous Machine Intelligence](https://openreview.net/pdf?id=BZ5aUm_I9_H)
- **Gary Marcus** - systematic critique of LLM limitations.
  [Rebooting AI (book)](https://www.penguinrandomhouse.com/books/603982/rebooting-ai-by-gary-marcus-and-ernest-davis/)
- **Ernest Davis** - formalization of common sense and physical knowledge.
  [Commonsense Reasoning (book)](https://www.morganclaypool.com/doi/abs/10.2200/S00105ED1V01Y200805AIM003)
- **Yejin Choi** - leading researcher on commonsense NLP, creator of [ATOMIC](https://arxiv.org/abs/1811.00146) knowledge graph and [AI2 Commonsense](https://allenai.org/research) benchmark suite. Possibly the most active current researcher in this specific area.
- **John McCarthy** & **Patrick Hayes** - original formulation of the frame problem (1969). ["Some Philosophical Problems from the Standpoint of Artificial Intelligence"](https://www.sciencedirect.com/science/article/pii/B9780934613033500131) - historically foundational.

---
## Related problems

- [Embodied intelligence](embodied-intelligence.md) - physical experience as a source of common sense
- [Robustness](robustness.md) - common sense as a mechanism for checking plausibility
- [Compositional generalization](compositional-generalization.md) - applying rules to new situations
- [[causal-reasoning]] - intuitive physics is essentially a causal model of the world: objects fall _because of_ gravity, not merely _correlated with_ it
- [[hierarchical-planning]] - any non-trivial plan requires predicting physical and social consequences of actions