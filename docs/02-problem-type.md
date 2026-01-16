# 02 – Problem Type: Single vs Multi-Target Learning (Learning Notes)

## Context
These notes reflect my understanding gained by studying a college-provided AI project.
I did not author the original implementation.

---

## Overview
The project is designed to support **two related supervised learning problem types**:
- single-target prediction
- multi-target (multi-output / multi-label) prediction

The same pipeline is reused for both, with differences abstracted at the data-model layer.

---

## Single-Target Learning
**Definition**
- One input sample → one target variable
- Standard supervised classification or regression

**Characteristics**
- Simpler training and evaluation
- Most classical ML models support this directly
- Metrics are straightforward (accuracy, precision/recall, etc.)

**Why it matters**
Single-target learning is often used as:
- a baseline
- a starting point before extending to more complex outputs

---

## Multi-Target / Multi-Label Learning
**Definition**
- One input sample → multiple target variables
- Targets may be correlated

**Challenges**
- Standard classifiers predict only one label
- Dependencies between labels can be important
- Evaluation becomes more complex

**Common strategies**
- Independent models per target
- Classifier Chains (predict labels sequentially)
- Ensemble-based approaches

---

## How This Project Handles the Difference
The project separates **problem type from model logic**:

- A **single-target data model** handles one output column
- A **multi-target data model** manages multiple outputs
- The rest of the pipeline (training, evaluation, saving results) remains unchanged

This design allows:
- switching between problem types via configuration
- reuse of modelling and evaluation code
- cleaner experimentation

---

## Key Learning Takeaways
- Multi-target learning is not just “more labels” — it changes modelling assumptions
- Abstracting problem type early simplifies system design
- Classifier chains and ensembles help capture label relationships
- Clean separation of concerns is critical in ML engineering
