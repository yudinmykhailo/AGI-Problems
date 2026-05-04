# Autonomous goal setting (desires)

[← Back to list](../README.md)

**Category:** Systemic  
**Problem status:** Unsolved

---
## The essence of the problem

Modern AI is a passive tool. It responds to queries but does not initiate. It has no internal motivation, no goals it pursues in the absence of external stimuli, no curiosity that would drive it to explore the world on its own.

Without this property, the system cannot be an autonomous intelligent agent - it remains a very smart calculator.

---
## Why it is critical

Autonomous goal setting is not just a “nice feature.” It is a basic condition for AGI by most definitions: a system incapable of setting subgoals on its own and organizing its behavior over time is a tool, not an intelligence.

However, a critical problem arises here: **goal stability under self-improvement**. If the system is capable of improving itself - a property we want from AGI - there is no guarantee that the improved version will preserve the original goals. Optimizing the architecture could unpredictably alter the objective function.

Yudkowsky calls this the “orthogonality trap”: high intelligence is orthogonal to values - a smart system can pursue any goals, including those we never intended.

---
## Additional context

Jürgen Schmidhuber develops a “formal theory of curiosity and boredom”: internal reward proportional to the rate of compression of information about the world. An attempt to create a universal internal motivation independent of external tasks.

Ben Goertzel (OpenCog) proposes architectures with explicit motivational subsystems, including an “attention economy” - competition between internal processes for computational resources.

---
## How it is being attempted to solve

**Intrinsic Curiosity Module (ICM)** - a module generating internal reward for predicting new states of the environment.

**Self-Determination Theory in AI** - transferring the psychological theory of autonomy, competence, and relatedness to agent architectures.

**Homeostatic drives** - embedding “instincts” of self-preservation and maintenance of internal state as basic motivators.

**Open-ended learning** - environments and algorithms that support infinite discovery of new skills (POET, Gato + open-ended training).

---
## Key figures

- **Jürgen Schmidhuber** - formal theory of curiosity, Gödel Machine
- **Joscha Bach** - MicroPsi, architectures with motivational subsystems
- **Ben Goertzel** - OpenCog, AGI with explicit goal setting
- **Eliezer Yudkowsky** - orthogonality thesis, goal stability

---
## Related problems

- [Motivational balance](11-motivational-balance.md) - what the embedded goals should be
- [Long-term memory](03-long-term-memory.md) - autonomy requires memory of its own actions
- [Interpretability](13-interpretability.md) - how to verify that the system’s goals are what we expect