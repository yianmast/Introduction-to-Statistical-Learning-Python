# Resampling Methods in Statistical Learning

## Summary

Resampling methods like cross-validation and the bootstrap are powerful tools to estimate model performance and prediction uncertainty. This project demonstrates how to:
- Implement k-fold and leave-one-out cross-validation.
- Estimate test error and model stability.
- Use the bootstrap to compute standard deviation of model predictions.
- Derive and simulate the probability of an observation being included in a bootstrap sample.

## Overview

Key examples include:
- Comparing bias-variance trade-offs of different cross-validation methods.
- Plotting the probability that a data point appears in a bootstrap sample as sample size increases.
- Numerical simulations to confirm theoretical results.
- Python visualizations and Monte Carlo estimation of bootstrap inclusion probability.

## Key Libraries Used

- `numpy` – efficient numerical computations and simulations.
- `matplotlib` – plotting results and probability curves.
- `scikit-learn` – model fitting and cross-validation utilities (optional).
- `random` or `numpy.random` – for bootstrap sampling.
