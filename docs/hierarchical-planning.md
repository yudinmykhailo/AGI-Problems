# Hierarchical Planning (Temporal Abstraction)

[← Back to overview](../README.md)

**Category:** Cognitive / Technical
**Status:** Unsolved

---
## The Problem

The ability to plan actions over vast time horizons is one of the most distinctive
features of human intelligence. A person can hold a goal for years — "finish a
PhD", "build a company", "raise a child" - while continuously decomposing it into
sub-goals, adjusting plans, and executing millions of low-level actions without
losing sight of the larger objective.

Current AI agents handle short planning chains well but progressively lose
coherence as planning depth increases. The deeper the hierarchy, the worse the
performance.

---
## Why It Matters

Without hierarchical planning, AGI cannot pursue complex, multi-year objectives -
from scientific research programs to infrastructure management to open-ended
exploration. Two specific failure modes arise:

**Goal dissolution**: as the system works through low-level actions, the original
high-level goal becomes diluted or forgotten. The agent gets lost in subproblems
and never returns to the top-level objective.

**Combinatorial explosion**: flat planning over long horizons requires evaluating
an astronomically large number of action sequences. Hierarchical abstraction is the
only known mechanism that makes long-horizon planning computationally tractable -
by reasoning at multiple levels of granularity simultaneously.

This is also directly connected to the problem of **autonomy**: a system that
cannot plan over long time horizons cannot be a genuine agent - it can only
react to immediate prompts.

---
## Additional Context

The Options Framework (Sutton, Precup, Singh, 1999) was the first formal
treatment of temporal abstraction in reinforcement learning: an "option" is a
closed-loop policy for taking actions over a period of time, with an initiation
set and a termination condition. This gave the field a mathematical foundation
for thinking about multi-level action hierarchies.

Cognitive science offers a complementary perspective: Miller, Galanter, and
Pribram's TOTE model (Test-Operate-Test-Exit, 1960) described hierarchical
goal structures in human cognition decades before modern AI. The insight that
intelligent behavior is inherently hierarchical is not new - but implementing it
robustly in learned systems remains unsolved.

Modern LLMs show surprisingly competent long-horizon behavior through chain-of-
thought prompting and multi-step reasoning - but this is not genuine hierarchical
planning; it is sequential text generation that mimics planning without an explicit
goal-state representation.

---
## Current Approaches

**Options Framework** - formalization of temporally extended actions in
reinforcement learning. Defines "options" as sub-policies with explicit start and
termination conditions.

**Hierarchical Reinforcement Learning (HRL)** - architectures with a "manager"
(sets subgoals) and a "worker" (executes primitive actions). Key examples: HIRO,
FeUdal Networks, MAXQ.

**Goal-Conditioned RL** - training agents to reach arbitrary goal states, enabling
compositional chaining of subgoals.

**Task and Motion Planning (TAMP)** - hybrid symbolic/continuous planning used in
robotics, combining discrete high-level task planning with continuous motion
planning.

**LLM-based planners** - using language models as high-level planners that
decompose goals into subtasks (ReAct, Plan-and-Solve, AutoGPT-style systems).
Promising in practice, but lack formal correctness guarantees.

---
## Key Persons and Works

- **Richard Sutton** - founder of reinforcement learning, Options Framework.
  [Between MDPs and semi-MDPs: A framework for temporal abstraction](https://www.sciencedirect.com/science/article/pii/S0004370299000446)
- **David Silver** - deep planning and AlphaGo/AlphaZero at DeepMind.
  [Mastering the game of Go with deep neural networks](https://www.nature.com/articles/nature16961)
- **Doina Precup** - co-author of Options Framework, temporal abstraction theory.
  [Temporal Abstraction in Reinforcement Learning (PhD thesis)](https://scholarworks.umass.edu/dissertations/AAI9978540)
- **Josh Tenenbaum** - hierarchical Bayesian models of planning in human cognition.
  [How to Grow a Mind](https://www.science.org/doi/10.1126/science.1192788)

---
## Related Problems

- [Autonomous Goal-Setting](goal-setting.md) - long-horizon planning requires
  stable intrinsic goals
- [Long-Term Memory](long-term-memory.md) - tracking progress toward distant goals
  requires episodic memory
- [Causal Reasoning](causal-reasoning.md) - predicting outcomes of multi-step
  action sequences requires causal models
- [Common Sense](common-sense.md) - decomposing goals into sensible subgoals
  requires implicit world knowledge