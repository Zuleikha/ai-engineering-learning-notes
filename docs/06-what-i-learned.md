# 06 – What I Learned (Learning Notes)

## Context
These reflections are based on studying and running a college-provided AI project
as part of the PG Diploma in AI.  
I did not author the original codebase.

---

## Understanding Multi-Target Learning
Before studying this project, my experience was primarily with single-target
classification and regression.

This project helped me understand that:
- multi-target learning is not just “more outputs”
- relationships between targets can matter
- modelling choices directly affect how those relationships are captured

Classifier chains, in particular, highlighted how label dependencies can be used
to improve predictions.

---

## Importance of Abstraction in ML Systems
One of the biggest takeaways was the value of **clean abstraction**.

Separating:
- data handling
- model logic
- configuration
- training and evaluation

made the system easier to understand, modify, and extend.

This reinforced that ML engineering is as much about **software design** as it is
about algorithms.

---

## Model Comparison Over Model Optimisation
Rather than tuning a single model, the project emphasised:
- comparing different algorithms
- understanding trade-offs
- evaluating ensembles versus individual models

This approach improved my intuition for when certain models are appropriate and
why ensembles are often used in practice.

---

## Evaluation and Reproducibility
The project reinforced the importance of:
- consistent evaluation across experiments
- saving outputs and trained models
- using configuration-driven pipelines

These practices are essential for reproducibility and are directly applicable to
real-world ML systems.

---

## From Coursework to Engineering Thinking
Studying this codebase helped bridge the gap between:
- academic ML exercises
- and production-style ML engineering

Key mindset shifts included:
- thinking in terms of pipelines, not scripts
- designing for experimentation
- prioritising clarity and structure

---

## How This Influences My Work Going Forward
As a result of this project, I now:
- design ML systems with clearer separation of concerns
- think explicitly about problem type early (single vs multi-target)
- favour reproducible, configuration-driven workflows
- evaluate multiple approaches before committing to a solution

These lessons directly inform how I approach my own AI and ML projects.
