# Formal Verification and Safety Guarantees

[← Back to overview](../README.md)

**Category:** Philosophical / Technical
**Status:** Unsolved at scale

---
## The Problem

Formal verification is the mathematical proof that a system behaves correctly
under all possible inputs and conditions - not just the ones tested. For
traditional software, such proofs exist: we can formally verify that a sorting
algorithm always produces a sorted output, or that a chip's logic gates behave
correctly.

For neural networks and AGI systems, we have no equivalent capability. We can
test, benchmark, and red-team - but we cannot *prove* that a system will behave
safely in all situations it might encounter.

---
## Why It Matters

The difference between testing and verification is the difference between
"we haven't found a failure yet" and "failures of this type are impossible."
For AGI deployed in critical systems - medical diagnosis, autonomous vehicles,
power grids, financial infrastructure - the first is not enough.

**The coverage problem.** Testing evaluates behavior on a finite set of inputs.
The space of possible real-world inputs is effectively infinite. No matter how
extensive the test suite, it cannot cover edge cases that were not anticipated
during evaluation.

**The distribution shift problem.** A system verified to behave safely on
training and test distributions may behave unsafely on inputs from a shifted
distribution encountered in deployment. Formal verification would need to
account for all possible distributions - currently impossible.

**The specification problem.** Formal verification requires a formal
specification of what "correct" behavior means. For narrow tasks (sort this
list, verify this circuit) specifications are tractable. For AGI-level tasks
("act in humanity's long-term interest") writing a formal specification is
itself an unsolved problem - equivalent to solving value learning.

**Stakes asymmetry.** A misaligned AGI that passes all tests but fails in
novel real-world situations has already been deployed and caused harm before
the failure is detected. Unlike software bugs, some AGI failures may be
irreversible.

---
## Additional Context

For classical software, formal methods (model checking, theorem proving,
abstract interpretation) have been successfully applied to safety-critical
systems: avionics, nuclear plant controllers, cryptographic protocols. The
CompCert verified C compiler and the seL4 verified microkernel are landmark
achievements.

Neural networks present a fundamentally different challenge. Their behavior
emerges from billions of floating-point parameters learned from data, not from
explicit logical rules that can be symbolically analyzed. The geometry of their
decision boundaries in high-dimensional space is extraordinarily complex.

**Neural network verification** is an active research area: tools like AI2,
Reluplex, and α,β-CROWN can verify properties of small networks (e.g.,
"for all inputs within ε of this image, the classification does not change").
But these methods scale poorly - verifying even a moderately sized network
can take hours, and they do not apply to the largest models.

---
## Current Approaches

**Satisfiability Modulo Theories (SMT) solvers** - encoding network behavior
as logical constraints and using automated theorem provers to verify properties.
Works for small networks; does not scale.

**Abstract interpretation** - over-approximating the set of possible network
outputs for a given input region. Faster than exact verification but produces
conservative bounds.

**Certified robustness** - proving that a network's prediction is stable within
a defined neighborhood of an input point. Randomized smoothing makes this
tractable for larger models at the cost of accuracy.

**Runtime monitoring** - rather than proving safety upfront, monitoring system
behavior at inference time and triggering fallbacks when uncertainty is high
or inputs are out-of-distribution.

**Formal specification languages** - research into how to write machine-readable
specifications of complex behavioral requirements, as a prerequisite to
verifying them.

---
## Key Figures and Works

- **Patrick Cousot** - inventor of abstract interpretation, the theoretical
  foundation of program analysis.
  [Abstract Interpretation: A Unified Lattice Model](https://dl.acm.org/doi/10.1145/512950.512973)
- **Guy Katz** - Reluplex, first practical SMT-based neural network verifier.
  [Reluplex: An Efficient SMT Solver for Verifying Deep Neural Networks](https://arxiv.org/abs/1702.01135)
- **Mykel Kochenderfer** - safety and verification for autonomous systems.
  [Algorithms for Decision Making](https://algorithmsbook.com/)
- **Stuart Russell** - formal approaches to safe AI behavior.
  [Research Priorities for Robust and Beneficial Artificial Intelligence](https://arxiv.org/abs/1602.03506)
- **Gerwin Klein** - seL4 verified microkernel, the gold standard for
  software verification.
  [seL4: Formal Verification of an OS Kernel](https://dl.acm.org/doi/10.1145/1629575.1629596)

---
## Related Problems

- [Robustness](robustness.md) - verification and robustness address the same
  failure mode from different angles: proof vs. empirical testing
- [Interpretability](interpretability.md) - understanding what a network computes
  is a prerequisite to formally specifying and verifying it
- [Value Learning](value-learning.md) - verification requires a formal
  specification; writing that specification is itself unsolved
- [Recursive Self-Improvement](recursive-self-improvement.md) - a self-modifying
  system invalidates any verification performed on a previous version