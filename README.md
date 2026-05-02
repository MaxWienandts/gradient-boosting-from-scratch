# Gradient Boosting from Scratch

This is a **mechanistic, bottom-up reconstruction** of Gradient Boosting.

The goal is to understand — in precise, operational terms — how Gradient Boosting actually works. We will build the method step by step, starting from its simplest components and progressively introducing the ideas that lead to a full Gradient Boosting Machine (GBM).

The dataset used here (Lending Club loan data) is **only a working example**. It provides a realistic, structured environment, but the focus of this notebook is entirely on the **learning algorithm**, not the domain.

---

## Learning Strategy

We follow a strict progression:

1. **Single Decision Tree**

   * How trees partition the feature space
   * Impurity minimization (regression/classification)
   * Limitations: high variance, instability

2. **Bagging**

   * Bootstrap sampling
   * Variance reduction through averaging
   * Why independent noisy learners can be powerful

3. **Random Forest**

   * Feature subsampling
   * Tree decorrelation as a variance control mechanism

4. **Gradient Boosting**

   * Additive modeling
   * Residual fitting as a learning signal
   * Functional gradient descent perspective
   * Learning rate (shrinkage) and sequential dependence

Each step is motivated by a concrete limitation of the previous one.

---

## Implementation Philosophy

All key components will be implemented **from scratch using NumPy/Pandas**. This includes:

* Tree splitting logic
* Bootstrap sampling
* Ensemble aggregation
* Residual computation and updates

We deliberately avoid high-level libraries (e.g., `scikit-learn`, `XGBoost`, `LightGBM`) during the learning phase.

---

## What You Should Expect

* Work through the **exact mechanics** of each algorithm
* See how ensemble methods emerge from simple ideas
* Understand Gradient Boosting as an **optimization procedure**, not just a model

By the end, you should be able to derive and implement a GBM independently.
