# Jaya-as-a-Modern-Hyperparameter-Optimization-Engine







GSoC 2026 – R Project for Statistical Computing (rstats)

This repository contains my prototype implementation for the GSoC 2026 idea:

“Jaya for Modern Hyperparameter Optimization”




The goal of this work is to extend the Jaya algorithm into a mixed-type hyperparameter optimization engine suitable for modern ML workflows.












Target Organization: R Project for Statistical Computing (rstats)
GSoC Idea: Jaya for Modern Hyperparameter Optimization
Proposed Mentor: Neeraj Bokde












Test Results : 

The prototype was validated across three progressively complex levels:
















1️.  Easy Level – Integer Hyperparameter Optimization

Task: Optimize max_depth of Decision Tree (Iris dataset)
Metric: 5-Fold Cross-Validation Accuracy





Observed Results:

Best Accuracy Achieved: 0.9667

Convergence achieved within first few iterations

Stable across multiple runs

Lower variance compared to Random Search baseline











2️.  Medium Level – Mixed-Type Optimization

Model: Random Forest
Hyperparameters Tuned:

n_estimators (Integer)

max_depth (Integer)

criterion (Categorical)

Validation Outcome:

Successful continuous-to-discrete decoding

Correct categorical embedding using argmax encoding

Stable convergence behavior

No runtime errors during mixed-type search




















3️.  Hard Level – Generic Jaya Tuning Engine

Implemented:

Functional jaya_tune() optimizer

Object-Oriented JayaOptimizer class

Bounded search support

Mixed-type decoding layer

Iterative improvement tracking

Performance Observations:

Convergence stability confirmed on classification tasks

Deterministic improvement toward best individual

Successfully handled normalized continuous search space














Current Status

 1. Integer-safe optimization implemented
2.  Mixed-type encoding layer implemented
3.  Generic optimizer engine developed
4.  Functional and OOP designs completed
5.  Initial benchmarking completed

This repository represents an initial working prototype toward building a production-ready Jaya-based HPO engine for integration into the R ecosystem
