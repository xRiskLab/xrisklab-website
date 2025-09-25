---
layout: project
title: "RFGBoost"
description: "Random Forest Gradient Boosting implementation combining ensemble methods"
image: "/assets/images/projects/rfgboost.png"
github: "https://github.com/xRiskLab/rfgboost"
pypi: "https://pypi.org/project/rfgboost/"
tags: ["Python", "XGBoost", "Scikit-learn", "Random Forest", "Machine Learning", "Ensemble"]
featured: false
---

RFGBoost combines **Random Forest with Gradient Boosting** using Weight of Evidence encoding for interpretable machine learning with categorical features.

## Key Features

- **Interpretable Boosting**: Uses Random Forest as base learners instead of single decision trees
- **Categorical Feature Mastery**: Built-in WOE encoding handles high-cardinality categories automatically
- **Uncertainty Quantification**: Built-in confidence intervals for risk-aware predictions
- **Dual Base Learners**: Choose between scikit-learn or XGBoost RandomForest implementations

## Best Used For

- **Financial Risk Modeling**: Credit scoring and risk management where interpretability is mandatory
- **Categorical-Heavy Datasets**: Datasets with many categorical features that need careful encoding
- **Regulatory Compliance**: Applications requiring clear decision paths and explainable predictions

*Perfect for data scientists who need gradient boosting performance with the interpretability that Random Forest provides, especially in regulated industries.*