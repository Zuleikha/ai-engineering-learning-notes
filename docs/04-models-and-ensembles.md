# 04 – Models and Ensembles (Learning Notes)

## Context
These notes reflect my understanding gained by studying a college-provided AI project.
I did not author the original model implementations.

---

## Overview
The project is designed to **compare multiple modelling strategies** rather than rely
on a single algorithm. This allows evaluation of trade-offs between different
classical machine learning approaches.

The models are implemented behind a shared interface, enabling consistent training
and evaluation.

---

## Individual Models
The following model families are explored in the project:

### Random Forest
- Ensemble of decision trees trained on bootstrapped samples
- Handles non-linear relationships well
- Robust to noisy features
- Often used as a strong baseline

### AdaBoost
- Sequential ensemble where each model focuses on previous errors
- Can improve performance on difficult samples
- Sensitive to noisy data

### Histogram-based Gradient Boosting
- Efficient gradient boosting implementation
- Scales well to larger datasets
- Handles complex feature interactions

### Stochastic Gradient Descent (SGD)
- Linear model trained with gradient-based optimisation
- Fast and scalable
- Useful as a lightweight baseline

---

## Multi-Target Modelling Strategies
Standard classifiers predict a single target. This project explores techniques to
extend them to **multi-target prediction**.

### Independent Models
- One model trained per target variable
- Simple but ignores relationships between targets

### Classifier Chains
- Targets are predicted sequentially
- Each prediction is used as input for the next
- Captures dependencies between labels

This approach is particularly useful when target variables are correlated.

---

## Ensemble Techniques
Beyond individual models, the project explores **ensembling strategies** to improve
robustness and performance.

### Random Trees Ensembling
- Combines predictions from multiple tree-based models
- Reduces variance
- Improves generalisation

### Voting Classifiers
- Aggregates predictions from multiple models
- Can be hard voting (majority) or soft voting (probability-based)
- Helps balance weaknesses of individual models

---

## Model Abstraction
All models inherit from a common base class.

This design:
- standardises training and prediction
- simplifies switching models via configuration
- avoids duplicated logic across implementations

It reflects good ML engineering practice.

---

## Key Learning Takeaways
- Different models excel under different data conditions
- Ensemble methods often outperform single models
- Classifier chains are powerful for multi-label problems
- Abstracting model logic improves experimentation speed
