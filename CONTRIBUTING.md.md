# Contributing to AGI Problems

Thank you for your interest in contributing! This repository aims to be a
rigorous, well-sourced reference on fundamental barriers to AGI — not a
collection of opinions or speculation.

---
## What belongs here

A problem belongs in this repository if it meets **all three** criteria:
1. **Fundamental** — it is a structural barrier, not an engineering detail.
   The problem cannot be solved simply by more compute, more data, or better
   software engineering.
2. **Unsolved or actively researched** — there is no consensus solution as of
   the current date. Problems that have been convincingly solved should be
   noted as such, not removed.
3. **Has serious academic or research attention** — there are published papers,
   named researchers, or active research programs addressing it.

---
## What does NOT belong here

- Engineering challenges that are hard but not fundamental (e.g. "training is
  expensive")
- Problems specific to a single modality or application (e.g. "image
  segmentation accuracy")
- Regulatory, legal, or political challenges around AI deployment
- Speculation without research backing

---
## How to propose a new problem

1. **Open an Issue** with the title `[New Problem] Your Problem Name`
2. In the issue body, answer these three questions:
   - What is the problem in one paragraph?
   - Why is it a *fundamental* barrier (not just an engineering challenge)?
   - Who are 2–3 researchers working on it, with links to their work?
3. If the issue gets a positive response, open a **Pull Request** with a new
   file in `docs/` following the template below.

---
## File template

Every problem page must follow this structure:

```markdown
# Problem Name

[← Back to overview](../README.md)

**Category:** Technical | Cognitive | Systemic | Philosophical
**Status:** Unsolved | Actively researched | Partially addressed

---
## The Problem

[2–4 paragraphs describing what the problem is]

---
## Why It Matters

[Why this is a *fundamental* barrier, not just a hard engineering problem]

---
## Additional Context

[Historical background, key experiments, analogies to human cognition]

---
## Current Approaches

[Named approaches with brief descriptions]

---
## Key Figures and Works

- **Name** — role/contribution.
  [Paper or book title](URL)

---
## Related Problems

- [Problem Name](filename.md) — one sentence on the connection
```