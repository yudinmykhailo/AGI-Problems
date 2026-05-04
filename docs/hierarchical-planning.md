# Hierarchical planning (Temporal Abstraction)

[← Back to list](../README.md)  
**Category:** Cognitive / Technical  
**Problem status:** Unsolved

---
## The essence of the problem

The ability to plan actions over vast time horizons. A human can hold a goal for years, breaking it down into millions of small actions. Current AI agents handle short chains well but lose the goal as planning depth increases.

---
## Why it is critical

Without hierarchical planning, AGI will not be able to realize complex multi-year projects - from scientific research to infrastructure management. The system will “get stuck” in low-level details and cannot efficiently reallocate resources among long-term tasks.

---
## How it is being attempted to solve

**Options Framework** - formalization of actions as temporal abstractions in reinforcement learning.  
**Hierarchical Reinforcement Learning (HRL)** - architectures with a “manager” (sets goals) and a “worker” (executes primitives).

---
## Key figures and works

- **Richard Sutton** - founder of reinforcement learning. [Between MDPs and semi-MDPs: A framework for temporal abstraction](https://www.sciencedirect.com/science/article/pii/S0004370299000446)  
- **David Silver** - work at DeepMind on deep planning.