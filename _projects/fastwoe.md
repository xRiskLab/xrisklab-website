---
layout: project
title: "FastWoe"
description: "Fast Weight of Evidence (WOE) encoding with statistical inference and confidence intervals"
image: "/assets/images/projects/fastwoe.png"
github: "https://github.com/xRiskLab/fastwoe"
pypi: "https://pypi.org/project/fastwoe/"
tags: ["Python", "Scikit-learn", "Statistics", "Feature Engineering", "Machine Learning"]
featured: true
---

FastWoe is a Python library for efficient **Weight of Evidence (WOE)** encoding of categorical features with rigorous statistical inference. Designed for machine learning practitioners who need both performance and interpretability in their feature engineering workflows.

## Key Features

- **⚡ Fast WOE Encoding**: Leverages scikit-learn's optimized algorithms for efficient computation
- **📊 Statistical Confidence Intervals**: Provides standard errors and confidence intervals for WOE values
- **🔍 IV Standard Errors**: Statistical significance testing for Information Value with confidence intervals
- **🎯 High-Cardinality Support**: Built-in preprocessing to handle categorical features with many categories
- **🔬 Intelligent Binning**: Support for decision tree-based binning and FAISS KMeans clustering
- **🔧 Sklearn Compatible**: Follows scikit-learn's preprocessing transformer interface

## What is Weight of Evidence?

Weight of Evidence (WOE) transforms categorical features into continuous, interpretable scores that measure the relationship strength between feature categories and target labels. It's particularly valuable in credit scoring and risk management where model interpretability is crucial.

**Key Benefits:**
- Handles missing values and rare categories gracefully
- Provides interpretable coefficients in logistic regression
- Enables statistical significance testing
- Industry standard in financial modeling

## Quick Example

```python
from fastwoe import FastWoe
import pandas as pd

# Your data
df = pd.DataFrame({
    'category': ['A', 'B', 'C'] * 100,
    'target': [0, 1, 1] * 100
})

# Apply WOE encoding
woe = FastWoe()
X_woe = woe.fit_transform(df[['category']], df['target'])

# Get confidence intervals
ci_results = woe.predict_ci(df[['category']], alpha=0.05)
```

## Use Cases

- **Credit Scoring**: Traditional scorecard development with statistical rigor
- **Risk Management**: Interpretable feature engineering for regulated industries
- **Model Validation**: Statistical significance testing for feature selection
- **Regulatory Compliance**: Transparent models with confidence intervals

---

*For detailed documentation and examples, visit the [GitHub repository](https://github.com/xRiskLab/fastwoe).*
