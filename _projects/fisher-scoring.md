---
layout: project
title: "Fisher Scoring"
description: "Efficient implementation of Fisher's scoring algorithm for maximum likelihood estimation"
image: "/assets/images/projects/fisher-scoring.png"
github: "https://github.com/xRiskLab/fisher-scoring"
pypi: "https://pypi.org/project/fisher-scoring/"
tags: ["Python", "Statistics", "Machine Learning", "Classification", "MLE"]
featured: false
---

# Fisher Scoring with Python

**Author:** [xRiskLab](https://github.com/xRiskLab)<br>
**License:** [MIT License](https://opensource.org/licenses/MIT) (2025)

[![CI](https://github.com/xRiskLab/fisher-scoring/workflows/CI/badge.svg)](https://github.com/xRiskLab/fisher-scoring/actions)
[![Compatibility](https://github.com/xRiskLab/fisher-scoring/workflows/Python%20Version%20Compatibility/badge.svg)](https://github.com/xRiskLab/fisher-scoring/actions)
[![PyPI version](https://img.shields.io/pypi/v/fisher-scoring.svg)](https://pypi.org/project/fisher-scoring/)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

![Title](https://github.com/xRiskLab/fisher-scoring/raw/main/docs/images/title.png)

This repository contains optimized Python implementations of the Fisher Scoring algorithm for various logistic regression models. With version 2.0, the core algorithms are now significantly faster due to optimized matrix operations and reduced memory usage, providing faster convergence for larger datasets.

```python
%pip install fisher-scoring
from fisher_scoring import LogisticRegression

# Binary Classification
model = LogisticRegression()
model.fit(X_train, y_train)
predictions = model.predict(X_test)
probabilities = model.predict_proba(X_test)
confidence_intervals = model.predict_ci(X_test)

model.summary()
model.display_summary()
```

## Overview

### Introduction

This repository contains a Python package with scikit-learn compatible implementations of the Fisher Scoring algorithm for various modeling problems.

The packages provides implementations of logistic regression (MLE for binary, multiclass, and binary imbalanced) for proportions (risk or prevalence), robust logistic regression for outlier-resistant classification, and Poisson and Negative Binomial regression for log-linear regression for incidence rates.

1. Binary classification problems: **Logistic Regression**.
2. Robust binary classification problems: **Robust Logistic Regression**.
3. Multi-class classification problems: **Multinomial Logistic Regression**.
4. Imbalanced classification problems: **Focal Loss Logistic Regression**.
5. Count modeling problems: **Poisson Regression** and **Negative Binomial Regression**.

### Fisher Scoring Algorithm

The Fisher Scoring algorithm is an iterative optimization technique that estimates maximum likelihood estimates by leveraging the expected or observed Fisher information matrix. This second-order optimization method allows to avoid the use of learning rates and provides more stable convergence compared to gradient descent.

There are two types of information matrices used in the Fisher Scoring algorithm:

* **Expected Information Matrix**: Relies on predicted probabilities, providing an efficient approximation for the information matrix.
* **Empirical Information Matrix**: Uses ground truth labels to calculate the information matrix, often resulting in more reliable inference metrics.

These information matrices are used to derive standard errors of estimates to calculate detailed model statistics, including Wald statistics, p-values, and confidence intervals at a chosen level.

Source: [Limitations of the Empirical Fisher Approximation for Natural Gradient Descent](https://arxiv.org/pdf/1905.12558).

### Implementation Notes

- **Multinomial Logistic Regression**  
  The `MultinomialLogisticRegression` model differs from standard statistical multinomial logistic regression by using all classes rather than $K - 1$. This approach allows multi-class classification problems to be converted to binary problems by calculating $1 - P_{Class=1}$.

- **Focal Loss Regression**  
  The `FocalLossRegression` class employs a non-standard focal log-likelihood function in its optimization process leveraging $\gamma$ to focus on difficult-to-classify examples.
  The focal loss function, originally developed for object detection, prioritizes difficult-to-classify examples—often the minority class—by reducing the contribution of easy-to-classify samples. It introduces a focusing parameter, *gamma*, which down-weights the influence of easily classified instances, thereby concentrating learning on challenging cases.

  Source: [Focal Loss for Dense Object Detection](https://arxiv.org/abs/1708.02002).

## Models

### Logistic Regression

The `LogisticRegression` class is a custom implementation of logistic regression using the Fisher scoring algorithm. It provides methods for fitting the model, making predictions, and computing model statistics, including standard errors, Wald statistics, p-values, and confidence intervals.

**Parameters:**
- `epsilon`: Convergence threshold for the algorithm.
- `max_iter`: Maximum number of iterations for the algorithm.
- `information`: Type of information matrix to use ('expected' or 'empirical').
- `use_bias`: Include a bias term in the model.
- `significance`: Significance level for computing confidence intervals.

**Methods:**
- `fit(X, y)`: Fit the model to the data.
- `predict(X)`: Predict target labels for input data.
- `predict_proba(X)`: Predict class probabilities for input data.
- `predict_ci(X)`: Predict class probabilities with confidence intervals.
- `get_params()`: Get model parameters.
- `set_params(**params)`: Set model parameters.
- `summary()`: Get a summary of model parameters, standard errors, p-values, and confidence intervals.
- `display_summary()`: Display a summary of model parameters, standard errors, p-values, and confidence intervals.

### Robust Logistic Regression

The `RobustLogisticRegression` class implements robust logistic regression using the Fisher scoring algorithm with epsilon-contamination for outlier resistance. This method down-weights observations that are unlikely under the main model, providing robustness against data contamination and outliers.

**Parameters:**
- `epsilon_contamination`: Contamination level (0 ≤ ε ≤ 1). Higher values provide more robustness but may reduce efficiency (default: 0.05).
- `contamination_prob`: Probability for contamination distribution (default: 0.5).
- `tol`: Convergence tolerance for parameter updates.
- `max_iter`: Maximum number of iterations for the algorithm.
- `information`: Type of information matrix to use ('expected' or 'empirical').
- `use_bias`: Include a bias term in the model.
- `significance`: Significance level for computing confidence intervals.

**Methods:**
- `fit(X, y)`: Fit the robust model to the data with automatic outlier down-weighting.
- `predict(X)`: Predict target labels for input data.
- `predict_proba(X)`: Predict class probabilities for input data.
- `predict_ci(X)`: Predict class probabilities with confidence intervals.
- `get_params()`: Get model parameters.
- `set_params(**params)`: Set model parameters.
- `summary()`: Get a summary of model parameters, standard errors, p-values, confidence intervals, and robust weights.
- `display_summary()`: Display a comprehensive summary including robustness metrics (epsilon contamination, average/minimum robust weights).

**Key Features:**
- **Outlier Resistance**: Automatic down-weighting of observations unlikely under the main model.
- **Robust Weights**: Access to individual observation weights showing outlier identification.
- **Fisher Scoring Framework**: Consistent with other models using both expected and empirical information matrices.
- **Statistical Inference**: Complete inference statistics with robust standard errors and confidence intervals.
- **Rich Output**: Beautiful formatted summaries with robust-specific metrics and diagnostics.

### Multinomial Logistic Regression

The `MultinomialLogisticRegression` class implements the Fisher Scoring algorithm for multinomial logistic regression, suitable for multi-class classification tasks.

**Parameters:**
- `epsilon`: Convergence threshold for the algorithm.
- `max_iter`: Maximum number of iterations for the algorithm.
- `information`: Type of information matrix to use ('expected' or 'empirical').
- `use_bias`: Include a bias term in the model.
- `significance`: Significance level for computing confidence intervals.
- `verbose`: Enable verbose output.

**Methods:**
- `fit(X, y)`: Fit the model to the data.
- `predict(X)`: Predict target labels for input data.
- `predict_proba(X)`: Predict class probabilities for input data.
- `predict_ci(X)`: Predict class probabilities with confidence intervals.
- `summary(class_idx)`: Get a summary of model parameters, standard errors, p-values, and confidence intervals for a specific class.
- `display_summary(class_idx)`: Display a summary of model parameters, standard errors, p-values, and confidence intervals for a specific class.

The algorithm is in a beta version and may require further testing and optimization to speed up matrix operations.

### Focal Loss Regression

The `FocalLossRegression` class implements the Fisher Scoring algorithm with focal loss, designed for imbalanced classification problems where the positive class is rare.

**Parameters:**
- `gamma`: Focusing parameter for focal loss.
- `epsilon`: Convergence threshold for the algorithm.
- `max_iter`: Maximum number of iterations for the algorithm.
- `information`: Type of information matrix to use ('expected' or 'empirical').
- `use_bias`: Include a bias term in the model.
- `verbose`: Enable verbose output.

**Methods:**
- `fit(X, y)`: Fit the model to the data.
- `predict(X)`: Predict target labels for input data.
- `predict_proba(X)`: Predict class probabilities for input data.
- `predict_ci(X)`: Predict class probabilities with confidence intervals.
- `get_params()`: Get model parameters.
- `set_params(**params)`: Set model parameters.
- `summary()`: Get a summary of model parameters, standard errors, p-values, and confidence intervals.
- `display_summary()`: Display a summary of model parameters, standard errors, p-values, and confidence intervals.

### Poisson Regression

The `PoissonRegression` class implements the Fisher Scoring algorithm for Poisson regression, suitable for modeling count data and incidence rates. Features robust matrix operations with automatic fallback to pseudo-inverse for numerical stability.

**Parameters:**
- `max_iter`: Maximum number of iterations for optimization.
- `epsilon`: Convergence tolerance.
- `use_bias`: Whether to include an intercept term.
- `offset`: Offset term for rate modeling (e.g., log exposure times).
- `significance`: Significance level for confidence intervals.
- `information`: Type of information matrix to use ('expected' or 'empirical').

**Methods:**
- `fit(X, y)`: Fit the model to the data.
- `predict(X, offset=None)`: Predict mean values with optional custom offset.
- `calculate_st_errors(X)`: Calculate standard errors for the coefficients.
- `summary()`: Get comprehensive model statistics including coefficients, standard errors, p-values, and confidence intervals.
- `display_summary()`: Display beautiful formatted summary with Rich styling.

**Key Features:**
- **Offset Support**: Full support for rate modeling with log exposure times.
- **Information Matrix Choice**: Both expected and empirical Fisher information matrices supported.
- **Robust Implementation**: Safe matrix inversion with automatic pseudo-inverse fallback.
- **Statistical Summaries**: Complete inference statistics with Wald tests and confidence intervals.
- **Validated Accuracy**: Mathematical correctness verified against statsmodels with machine precision accuracy.

### Negative Binomial Regression

The `NegativeBinomialRegression` class implements the Fisher Scoring algorithm for Negative Binomial regression, suitable for overdispersed count data. Features enhanced robustness with comprehensive statistical inference and fixed critical implementation bugs.

**Parameters:**
- `max_iter`: Maximum number of iterations for optimization.
- `epsilon`: Convergence tolerance.
- `use_bias`: Whether to include an intercept term.
- `alpha`: Fixed dispersion parameter (overdispersion adjustment).
- `phi`: Constant scale parameter.
- `offset`: Offset term for the linear predictor.
- `significance`: Significance level for confidence intervals.
- `information`: Type of information matrix to use ('expected' or 'empirical').

**Methods:**
- `fit(X, y)`: Fit the model to the data.
- `predict(X, offset=None)`: Predict mean values with proper offset handling.
- `calculate_st_errors(X)`: Calculate standard errors with corrected implementation.
- `summary()`: Get comprehensive model statistics including coefficients, standard errors, p-values, and confidence intervals.
- `display_summary()`: Display beautiful formatted summary with Rich styling.

**Key Improvements:**
- **Fisher Scoring Conversion**: Converted from IWLS to proper Fisher scoring for consistency.
- **Information Matrix Choice**: Both expected and empirical Fisher information matrices supported (empirical recommended for numerical stability).
- **Bug Fixes**: Fixed missing offset in prediction and standard error calculations.
- **Robust Implementation**: Safe matrix inversion with automatic pseudo-inverse fallback.
- **Statistical Summaries**: Complete inference statistics with Wald tests and confidence intervals.
- **Enhanced Reliability**: Comprehensive testing ensures mathematical correctness.

## Utilities

### Visualization

The package includes a utility function for visualizing observed vs predicted probabilities for count data, which can be useful for users working with Poisson and Negative Binomial models.

**Function:**
- `plot_observed_vs_predicted(y, mu, max_count=15, alpha=None, title="Observed vs Predicted Probabilities", model_name="Model", ax=None, plot_params=None)`: Plot observed vs predicted probabilities for count data.

**Parameters:**
- `y`: Observed count data.
- `mu`: Predicted mean values from the model.
- `max_count`: Maximum count to consider for probabilities.
- `alpha`: Overdispersion parameter for Negative Binomial. If None, assumes Poisson (alpha=0).
- `title`: Title for the plot.
- `model_name`: Name of the model for labeling.
- `ax`: Matplotlib axis to plot on.

## 📝 Changelog

For a changelog, see [CHANGELOG](CHANGELOG.md).

> [!NOTE]  
> This package is in a beta release mode. The API is not considered stable for production use.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.