# Embodied intelligence

[← Back to list](../README.md)

**Category:** Technical  
**Problem status:** Unsolved

---
## The essence of the problem

Knowledge about the physical world obtained only through text remains fundamentally incomplete. AI can describe that ice is cold, glass is brittle, and fire burns - but it has never felt any of this.

This is not just a matter of “inexperience.” It is a fundamental architectural problem: a mind without a body forms a fundamentally different, truncated model of reality.

---
## Why it is critical

**The Symbol Grounding Problem** (Stevan Harnad, 1990): Symbols have meaning only if they are “grounded” - linked to sensory experience. The word “hot” for a language model is statistics of co-occurrence with other words. For a human - it’s a memory of a burn, the smell of burning, a reflex to pull back a hand. The difference is not quantitative but qualitative.

This means that AI’s reasoning about the physical world will always have hidden blind spots - it does not know what it does not know, because some classes of knowledge are unattainable without a body.

---
## Additional context

Yann LeCun argues that most human knowledge is acquired not through language but through sensorimotor interaction with the world in early childhood - before the child learns to speak. LLMs are trained on what can be written down, and they miss this entire foundational layer.

Sergey Levine (UC Berkeley) shows in robotics experiments that agents with physical bodies learn manipulation qualitatively differently and faster than agents trained only on video or descriptions.

---
## How it is being attempted to solve

**Robotic platforms** - learning in a physical body with sensory feedback (Boston Dynamics, Figure AI, physical simulators like MuJoCo).

**Photorealistic simulators** - NVIDIA Isaac, DeepMind Lab, Habitat (Meta). Allow accumulating physical experience cheaper than in reality.

**Multimodal models** - GPT-4V, Gemini - integration of visual and linguistic experience as a step toward a more complete world model.

**World Models (LeCun)** - learning an internal predictive model of the world’s physics without explicitly programming the laws.

---
## Key persons and works

- **Yann LeCun** - author of world models concept, critic of purely linguistic approaches
- **Sergey Levine** - robotics and reinforcement learning in physical agents
- **Stevan Harnad** - author of the Symbol Grounding Problem
- **Rodney Brooks** - pioneer of embodied AI, critic of GOFAI

---
## Related problems

- [Common sense](10-common-sense.md) - physical intuitions as part of common sense
- [Long-term memory](03-long-term-memory.md) - sensory experience requires episodic memory
- [Meta-learning](06-meta-learning.md) - learning through interaction