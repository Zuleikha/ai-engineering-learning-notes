# 05 – Training and Evaluation (Learning Notes)

## Context
These notes document my understanding gained by studying a college-provided AI project.
I did not author the original implementation.

---

## Overview
The project is structured to support **repeatable training and consistent evaluation**
across multiple models and problem types (single-target and multi-target).

The emphasis is on comparison and experimentation rather than optimising a single model.

---

## Training Flow
At a high level, training follows these steps:

1. Load configuration settings
2. Prepare features and target variables
3. Initialise the selected model or ensemble
4. Train the model on the training dataset
5. Generate predictions on held-out data

By centralising this flow, the same process can be reused across different modelling strategies.

---

## Configuration-Driven Training
Key training decisions are controlled via configuration, including:
- choice of model
- single-target vs multi-target mode
- data paths
- output locations

This allows experiments to be repeated or modified without changing core code.

---

## Evaluation Approach
Model performance is assessed after training using appropriate evaluation metrics.

Key considerations include:
- using the same evaluation process for all models
- enabling fair comparison between approaches
- supporting both single and multi-target outputs

Evaluation results are written to output files for later inspection.

---

## Outputs and Artifacts
The training process produces two main outputs:

- **Prediction / evaluation results**  
  Stored in a CSV file for analysis and comparison

- **Saved models**  
  Persisted to disk to allow reuse without retraining

This mirrors real-world ML workflows where models and results are treated as artifacts.

---

## Why This Matters
From an engineering perspective:
- separating training from evaluation improves clarity
- saving artifacts supports reproducibility
- configuration-driven pipelines reduce accidental errors

These patterns are common in production ML systems.

---

## Key Learning Takeaways
- Consistent evaluation is critical when comparing models
- Configuration-driven design supports experimentation
- Persisting models and results enables reproducibility
- Training pipelines should be reusable, not model-specific
