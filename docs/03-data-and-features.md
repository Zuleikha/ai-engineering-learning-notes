# 03 – Data and Feature Handling (Learning Notes)

## Context
These notes document my understanding of how data and features are handled in a
college-provided AI project. I did not author the original implementation.

---

## Data Sources
The project works with **structured tabular datasets**, provided as CSV files.

Examples observed include:
- application-related data
- purchasing or behavioural data

These datasets contain a mixture of:
- numeric features
- categorical features
- one or more target columns

---

## Data Loading
Data is loaded from disk early in the pipeline and passed through a consistent
interface so that different datasets can be swapped without changing the rest of the system.

This separation allows:
- reproducible experiments
- easier debugging
- clear ownership of data handling logic

---

## Feature Preparation
Before modelling, raw data must be converted into a form suitable for machine learning.

Typical steps include:
- handling missing values
- encoding categorical variables
- normalising or scaling numeric features
- separating features (`X`) from targets (`y`)

The exact preprocessing steps are abstracted away from the modelling code.

---

## Embeddings
The presence of an `embeddings` module suggests support for **vector representations**
of certain features (for example, text-based fields).

Embeddings:
- transform complex inputs into numerical vectors
- allow models to operate on richer representations
- are handled as part of feature preparation rather than modelling

---

## Why Feature Handling Matters
Poor feature preparation often limits model performance more than algorithm choice.

From studying this project, it is clear that:
- feature handling is treated as a first-class concern
- preprocessing is separated from training logic
- the pipeline is designed to support experimentation

---

## Key Learning Takeaways
- Clean feature pipelines make modelling more flexible
- Separating data handling reduces coupling in ML systems
- Embeddings are part of feature engineering, not model logic
- Well-structured data code improves reproducibility and clarity
