---
layout: project
title: "WoeBoost"
description: "Interpretable gradient boosting with WOE-based scoring for high-stakes domains"
image: "/assets/images/projects/woeboost.png"
github: "https://github.com/xRiskLab/woeboost"
pypi: "https://pypi.org/project/woeboost/"
tags: ["Python", "Machine Learning", "Interpretability", "Credit Scoring", "Gradient Boosting"]
featured: false
---

WoeBoost is a Python package designed to bridge the gap between the predictive power of gradient boosting and the interpretability required in high-stakes domains such as finance, healthcare, and law. It introduces an interpretable, evidence-driven framework for scoring tasks, inspired by the principles of **Weight of Evidence (WOE)** and the ideas of **Alan M. Turing**.

## Key Features

- **🌟 Gradient Boosting with Explainability**: Combines the strength of gradient boosting with the interpretability of WOE-based scoring systems
- **📊 Calibrated Scores**: Produces well-calibrated scores essential for decision-making in regulated environments
- **🤖 AutoML-like Enhancements**: Infers monotonic relationships automatically and supports early stopping
- **🔧 Support for Missing Values & Categorical Inputs**: Handles various data types seamlessly while maintaining interpretability
- **🛠️ Diagnostic Toolkit**: Partial dependence plots, feature importance analysis, and decision boundary visualization
- **📈 WOE Inference Maker**: Provides classical WOE calculations and bin-level insights

## How It Works

1. **🔍 Initialization**: Starts with prior log odds, representing baseline probabilities
2. **📈 Iterative Updates**: Each boosting iteration calculates residual per each binned feature and sums residuals into total evidence (WOE), updating predictions
3. **🔗 Evidence Accumulation**: Combines evidence from all iterations, producing a cumulative and interpretable scoring model

## Why WoeBoost?

- **💡 Interpretability**: Every model step adheres to principles familiar to risk managers and data scientists
- **✅ Alignment with Regulatory Requirements**: Calibrated and interpretable results meet the demands of high-stakes applications
- **⚡ Flexibility**: Works seamlessly with diverse data types and supports concurrency for feature binning

## Quick Start

### Training and Inference
```python
from woeboost import WoeBoostClassifier

# Initialize the classifier
woe_model = WoeBoostClassifier(infer_monotonicity=True)

# Fit the model
woe_model.fit(X_train, y_train)

# Predict probabilities and scores
probas = woe_model.predict_proba(X_test)[:, 1]
preds = woe_model.predict(X_test)
scores = woe_model.predict_score(X_test)
```

### WOE Inputs for Logistic Regression
```python
from woeboost import WoeBoostClassifier

# Initialize the classifier
woe_model = WoeBoostClassifier(infer_monotonicity=True)

# Fit the model
woe_model.fit(X_train, y_train)

# Transform features to WOE values
X_woe_train = woe_model.transform(X_train)
X_woe_test = woe_model.transform(X_test)
```

## Free-Threaded Python Support

WoeBoost includes experimental support for free-threaded Python builds, providing significant performance improvements:

- **3.67× speedup** for WoeBoost training with Python 3.14+freethreaded
- **Optimal performance at 8 threads** (vs 4 with GIL)
- **Tested on Python 3.14.0a5+freethreaded** (experimental builds)

### Installation with Free-Threaded Support
```bash
# Install free-threaded Python
uv python install 3.14.0a5+freethreaded

# Install WoeBoost with free-threaded dependencies
pip install woeboost[freethreaded]
```

## Installation

### Standard Installation
```bash
pip install woeboost
```

### Free-Threaded Python Support (Experimental)
```bash
# Install with free-threaded dependencies
pip install woeboost[freethreaded]
```

## Performance Benefits

- **3.67× faster training** - real measured performance improvement
- **Automatic thread optimization** (8 threads vs 4 with GIL)
- **No code changes required** - WoeBoost auto-detects free-threading
- **Same results, faster computation** - identical convergence, 3.67× speedup

## Use Cases

- **Credit Risk Modeling**: Interpretable scoring systems for financial institutions
- **Healthcare Risk Assessment**: Transparent models for medical decision support
- **Regulatory Compliance**: Models that meet explainability requirements
- **High-Stakes Decision Making**: Any domain requiring both accuracy and interpretability

## Documentation

For detailed documentation, technical notes, and API reference, visit the [WoeBoost GitHub repository](https://github.com/xRiskLab/woeboost).

## License

This project is licensed under the MIT License.
