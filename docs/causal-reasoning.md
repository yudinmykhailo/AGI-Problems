# Causal reasoning

[← Back to list](../README.md)

**Category:** Cognitive  
**Problem status:** Actively researched

---
## The essence of the problem

Modern neural networks are powerful machines for finding statistical patterns. They answer the question “How often do X and Y co-occur?” But they do not answer “Why does X cause Y?” or “What would happen if I intervene on X?”

This is the difference between correlation and causation - and it is critical for decision-making in the real world.

---
## Why it is critical

Judea Perl distinguishes three levels of causal reasoning (Ladder of Causation):

1. **Seeing** - “How often are people who take aspirin healthy?” - this is what LLMs can do.
2. **Doing** - “What happens if I give the patient aspirin?” - answering requires a causal model.
3. **Imagining** (counterfactual) - “Would the patient have recovered if I had not given aspirin?” - requires an even deeper model.

AGI systems incapable of rising above the first level will make critical mistakes when conditions change - even if they worked well in familiar situations.

**Abductive reasoning** - another missing layer. The ability to infer the most plausible hypothesis from incomplete data. This is how Sherlock Holmes works: from footprints on shoes to a biography. It is how a doctor diagnoses from symptoms. Current models struggle with this type of reasoning.

---
## Additional context

Yoshua Bengio argues that the next breakthrough in AI will require integrating causal reasoning into deep neural networks - what he calls “System 2 deep learning.” Current models work primarily in “System 1” mode - fast associative responses without reflection.

---
## How it is being attempted to solve

**Do-calculus (Pearl)** - a mathematical framework for reasoning about interventions and counterfactual scenarios. Allows formal distinction between correlation and causation.

**Causal Discovery** - algorithms for automatic extraction of causal graphs from data (PC algorithm, GES, NOTEARS).

**Structural Causal Models (SCM)** - explicit encoding of causal mechanisms into the model.

**Interventional training** - training models on data with explicit interventions, not just observations.

---
## Key persons and works

- **Judea Pearl** - author of do-calculus, Turing Award 2011
- **Yoshua Bengio** - integration of causality into neural networks
- **Bernhard Schölkopf** - causal representation in machine learning
- **Elias Bareinboim** - transportability of causal inferences

---
## Related problems

- [Common sense](10-common-sense.md) - intuitive physics as a causal model of the world
- [Robustness](05-robustness.md) - causal features are more robust than correlational ones
- [Theory of Mind](07-theory-of-mind.md) - intentions as causes of actions