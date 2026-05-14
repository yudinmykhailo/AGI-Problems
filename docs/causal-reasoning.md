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

**Example of AI’s failure to determine cause and effect: Asthma as a "protective factor"**

A neural network trained to predict mortality risk in pneumonia patients learned a dangerous spurious correlation: patients with asthma had _lower_ predicted mortality than average. The model was technically correct on training data - asthmatic patients with pneumonia are hospitalized more aggressively and monitored more closely, so they actually die less often in the dataset. But the cause was the clinical protocol, not the disease itself.

A model that learned causation would represent this correctly: asthma → aggressive treatment → lower mortality. A model that learned correlation concluded: asthma → lower risk → send home.

When deployed, such a model would recommend _less_ intensive care for a high-risk group - precisely because it could not distinguish "Y follows X in the data" from "X causes Y."

> Source: Caruana et al., "Intelligible Models for HealthCare" (KDD 2015) - the original case study from a real clinical risk prediction system.
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

- **Judea Pearl** - do-calculus, Turing Award 2011.
  [The Book of Why](http://bayes.cs.ucla.edu/WHY/)
- **Yoshua Bengio** - integration of causality into neural networks.
  [Towards Causal Representation Learning](https://arxiv.org/abs/2102.11107)
- **Bernhard Schölkopf** - causal representation learning.
  [Causality for Machine Learning](https://arxiv.org/abs/1911.10500)
- **Elias Bareinboim** - transportability of causal inference.
  [Causal Inference and the Data-Fusion Problem](https://www.pnas.org/doi/10.1073/pnas.1510507113)

---
## Related problems

- [Common sense](common-sense.md) - intuitive physics as a causal model of the world
- [Robustness](robustness.md) - causal features are more robust than correlational ones
- [Theory of Mind](theory-of-mind.md) - intentions as causes of actions