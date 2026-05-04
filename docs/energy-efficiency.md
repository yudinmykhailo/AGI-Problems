# Energy efficiency

[← Back to list](../README.md)

**Category:** Technical  
**Problem status:** Partially resolved

---
## The essence of the problem

The human brain consumes about 20 watts - roughly as much as a dim light bulb. At the same time, it solves problems of perception, language, planning, and social interaction simultaneously, in real time, for decades.

Modern large language models consume megawatts for training and kilowatts for inference. GPT-4, by various estimates, requires tens of thousands of times more energy per “act of thought” than the human brain.

---
## Why it is critical

There are two interrelated constraints.

**Physical.** The current transformer architecture requires multiplying giant matrices at each token. This is a fundamental computational action not optimizable without a change in architecture.

**Economic - scaling ceiling.** Empirically, doubling computational resources yields only a linear increase in model quality. This means that to achieve a qualitative leap, not just a larger cluster is needed - a different principle of computation is needed.

For autonomous AGI (e.g., embedded in a robot or operating without constant connection to a data center), the current energy profile makes the task physically unrealizable.

---
## Additional context

Biological neurons work differently: they are silent most of the time and only “fire” upon significant changes in the input signal (sparse activation). This dramatically reduces average energy costs. Moreover, in the brain, computation and memory are physically co-located - there is no constant movement of data between processor and memory, which is the main source of energy consumption in the traditional von Neumann architecture.

---
## How it is being attempted to solve

**Neuromorphic chips** - processors that mimic the operating principle of biological neurons. Intel Loihi 2 and IBM NorthPole implement computation “in place” and sparse activation.

**Spiking Neural Networks (SNN)** - networks where activation occurs only when the signal changes, not continuously.

**Mixture of Experts (MoE)** - an architecture where only a subset of model parameters is activated for each request. GPT-4 and Mixtral use this approach.

**Quantization and distillation** - compressing the model with minimal loss of quality to reduce hardware requirements during inference.

---
## Key figures and works

- **Intel team (Loihi)** - next-generation neuromorphic chips. [Intel Loihi 2](https://www.intel.com/content/www/us/en/research/neuromorphic-computing-loihi-2-brief.html)
- **IBM team (NorthPole)** - architecture without separation of memory and computation. [IBM NorthPole Research](https://research.ibm.com/blog/northpole-ibm-ai-chip)
- **Carver Mead** - founder of neuromorphic computing. [Analog VLSI and Neural Systems](https://archive.org/details/analogvlsineural0000mead)
- **Wolfgang Maass** - theorist of spiking neural networks. [Networks of Spiking Neurons](https://pubmed.ncbi.nlm.nih.gov/9310302/)

---
## Related problems

- [Meta-learning](06-meta-learning.md) - efficiency of learning, not just inference
- [Embodied intelligence](04-embodied-intelligence.md) - autonomous systems require low power consumption