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

Fisher Scoring provides **optimized implementations of the Fisher scoring algorithm** for maximum likelihood estimation across multiple statistical models.

## What It Does

Implements Fisher's second-order optimization method for various statistical models, offering faster convergence and more stable parameter estimation than gradient descent. Provides comprehensive statistical inference with confidence intervals and significance tests.

## Key Capabilities

- **Multiple Model Types**: Binary/multinomial logistic, robust logistic, focal loss, Poisson, and negative binomial regression
- **Statistical Inference**: Complete statistical summaries with standard errors, p-values, and confidence intervals  
- **Information Matrix Options**: Both expected and empirical Fisher information matrices supported
- **Robust Methods**: Outlier-resistant models with epsilon-contamination for data quality issues

## Best Used For

- **Statistical Modeling**: When you need proper statistical inference beyond just predictions
- **Robust Classification**: Handling datasets with outliers or contamination using robust logistic regression
- **Imbalanced Data**: Focal loss implementation for rare positive class problems
- **Count Data**: Poisson and negative binomial models for rate and frequency modeling
- **Regulatory Analysis**: Full statistical summaries required for compliance and validation

*Essential for statisticians and data scientists who need rigorous statistical inference, not just predictive performance.*

