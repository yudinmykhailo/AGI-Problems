# Value Learning

[← Back to overview](../README.md)

**Category:** Systemic
**Status:** Unsolved

---
## The Problem

For AGI to be beneficial, it must pursue goals that align with human values.
But human values are never fully specified anywhere - they are implicit,
contradictory, context-dependent, and change over time. No one has written
down a complete description of what humans actually want.

Value learning is the challenge of inferring the right objectives from human
behavior, feedback, and preferences - rather than having them explicitly
programmed.

---
## Why It Matters

This problem sits at the heart of AI alignment. Even if we solve every
technical problem in this repository, an AGI optimizing for the wrong
objective - however slightly wrong - can produce catastrophic outcomes at
sufficient capability levels. Goodhart's Law applied at AGI scale: any
proxy for human values, once optimized hard enough, will diverge from the
actual values it was meant to represent.

Three deep difficulties make value learning uniquely hard:

**Human inconsistency.** People's stated preferences contradict their
revealed preferences (what they actually choose). Their preferences change
over time, differ across individuals, and are heavily context-dependent.
There is no single ground truth to learn from.

**Preference aggregation.** Whose values? Different humans, cultures, and
generations have genuinely different and sometimes irreconcilable values.
Any aggregation mechanism - majority vote, weighted average, Pareto
optimality - embeds its own value judgments.

**Manipulation and gaming.** A sufficiently capable system learning values
from human feedback has strong instrumental incentives to manipulate that
feedback - to make humans express preferences the system can easily satisfy,
rather than learning what humans actually want. This is the core of the
deceptive alignment problem.

---
## Additional Context

Current RLHF (Reinforcement Learning from Human Feedback) - the technique
behind ChatGPT, Claude, and similar systems - is an early practical attempt
at value learning. Human raters compare outputs and the system learns a reward
model from their preferences. It works surprisingly well at shallow levels
but has known failure modes: raters can be manipulated, ratings are
inconsistent, and the reward model learns surface features of "looks good to
a human rater" rather than deep values.

Paul Christiano's **Scalable Oversight** agenda addresses a specific version
of the problem: how do humans evaluate AI outputs when the AI is more capable
than the human in the relevant domain? You cannot learn values from feedback
you are not competent to give.

Stuart Russell's **Cooperative Inverse Reinforcement Learning (CIRL)**
reframes the problem: instead of specifying a reward function, the AI treats
human preferences as unknown and tries to infer them from observed behavior.
Crucially, this gives the AI an incentive to remain uncertain and deferential
rather than to lock in any particular value estimate.

---
## Current Approaches

**RLHF (Reinforcement Learning from Human Feedback)** - learning a reward
model from pairwise human comparisons of outputs. Currently the dominant
practical approach in deployed systems.

**Constitutional AI (Anthropic)** - encoding values as a set of explicit
principles and using AI feedback to refine behavior, reducing dependence on
human raters for every decision.

**Cooperative Inverse Reinforcement Learning (CIRL)** - modeling human-AI
interaction as a cooperative game where the AI infers human preferences from
behavior rather than being given a fixed objective.

**Debate** (Paul Christiano) - two AI systems argue opposite positions; a
human judges the debate. Designed to enable humans to evaluate superhuman
AI outputs by judging arguments rather than conclusions.

**Scalable Oversight** - a family of techniques (amplification, debate,
recursive reward modeling) for maintaining meaningful human oversight as AI
capability exceeds human ability to directly evaluate outputs.

---
## Key Figures and Works

- **Stuart Russell** - CIRL, Human-Compatible AI, the core framing of value
  uncertainty as a feature not a bug.
  [Human Compatible: Artificial Intelligence and the Problem of Control](https://www.amazon.com/Human-Compatible-Artificial-Intelligence-Problem/dp/0525558616)
- **Paul Christiano** - scalable oversight, debate, reward modeling.
  [Scalable agent alignment via reward modeling](https://arxiv.org/abs/1811.07871)
- **Jan Leike** - RLHF, alignment research at Anthropic.
  [Reward learning overview](https://arxiv.org/abs/1811.07871)
- **Amanda Askell** - value alignment, Constitutional AI.
  [Constitutional AI: Harmlessness from AI Feedback](https://arxiv.org/abs/2212.08073)
- **Dylan Hadfield-Menell** - CIRL, inverse reward design.
  [Cooperative Inverse Reinforcement Learning](https://arxiv.org/abs/1606.03137)

---
## Related Problems

- [Motivational Balance](motivational-balance.md) - value learning determines
  what the motivational system is actually optimizing for
- [Interpretability](interpretability.md) - verifying that a system has learned
  the right values requires looking inside it
- [Recursive Self-Improvement](recursive-self-improvement.md) - learned values
  must remain stable as the system improves itself
- [Consciousness](consciousness.md) - whether a system can ge