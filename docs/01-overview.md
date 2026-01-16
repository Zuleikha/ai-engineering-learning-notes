# 01 – Project Overview (Learning Notes)

## Context
These notes are based on studying a **college-provided AI project** from the module  
**Engineering and Evaluating Artificial Intelligence (PGDAI)** at the National College of Ireland.

I did not design or author the original codebase.  
This document captures **my understanding** of the system architecture, modelling approach, and design decisions, for learning purposes only.

---

## What the Project Is
The project is a **machine learning system designed to support both single-target and multi-target prediction**, using a range of classical ML models and ensemble strategies.

The focus is not on a single model, but on:
- comparing modelling approaches
- handling multi-output prediction
- structuring an ML codebase for experimentation and evaluation

---

## Problem Type
The system supports two related problem types:

### 1. Single-target prediction
- One input → one target variable
- Standard supervised learning setup

### 2. Multi-target / multi-label prediction
- One input → multiple target variables
- Requires specialised strategies (e.g. classifier chains, ensembles)

The project abstracts these differences so the rest of the pipeline can remain consistent.

---

## High-level Architecture
At a high level, the system follows this flow:

