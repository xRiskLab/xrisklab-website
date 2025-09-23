---
layout: project
title: "FastWoe"
description: "Fast Weight of Evidence (WOE) encoding with statistical inference and confidence intervals"
github: "https://github.com/xRiskLab/fastwoe"
pypi: "https://pypi.org/project/fastwoe/"
---

FastWoe is a Python library for efficient **Weight of Evidence (WOE)** encoding of categorical features and statistical inference. It's designed for machine learning practitioners seeking robust, interpretable feature engineering and likelihood-ratio-based inference for binary classification problems.

## Key Features

- **Fast WOE Encoding**: Leverages scikit-learn's `TargetEncoder` for efficient computation
- **Statistical Confidence Intervals**: Provides standard errors and confidence intervals for WOE values
- **IV Standard Errors**: Statistical significance testing for Information Value with confidence intervals
- **Cardinality Control**: Built-in preprocessing to handle high-cardinality categorical features
- **Intelligent Numerical Binning**: Support for traditional binning, decision tree-based binning, and FAISS KMeans clustering
- **Compatible with scikit-learn**: Follows scikit-learn's preprocessing transformer interface

## What is Weight of Evidence?

Weight of Evidence (WOE) is a statistical technique that:

- Transforms discrete features into logarithmic scores
- Measures the strength of relationship between feature categories and true labels
- Provides interpretable coefficients as weights in logistic regression models
- Handles missing values and rare categories gracefully

**Mathematical Definition:**
```
WOE = ln(P(Event|Category) / P(Non-Event|Category)) - ln(P(Event) / P(Non-Event))
```

## Quick Start

```python
import pandas as pd
import numpy as np
from fastwoe import FastWoe, WoePreprocessor

# Create sample data
data = pd.DataFrame({
    'category': ['A', 'B', 'C'] * 100 + ['D'] * 50,
    'high_card_cat': [f'cat_{i}' for i in np.random.randint(0, 50, 350)],
    'target': np.random.binomial(1, 0.3, 350)
})

# Step 1: Preprocess high-cardinality features (optional)
preprocessor = WoePreprocessor(max_categories=10, min_count=5)
X_preprocessed = preprocessor.fit_transform(
    data[['category', 'high_card_cat']],
    cat_features=['high_card_cat']
)

# Step 2: Apply WOE encoding
woe_encoder = FastWoe()
X_woe = woe_encoder.fit_transform(X_preprocessed, data['target'])

print("WOE-encoded features:")
print(X_woe.head())
```

## Advanced Features

### Probability Predictions
```python
# Get predictions with Naive Bayes classification
preds = woe_encoder.predict_proba(X_preprocessed)[:, 1]
```

### Confidence Intervals
```python
# Get predictions with confidence intervals
ci_results = woe_encoder.predict_ci(X_preprocessed, alpha=0.05)
print(ci_results[['prediction', 'lower_ci', 'upper_ci']].head())
```

### Information Value Analysis
```python
# Get IV analysis with confidence intervals
iv_analysis = woe_encoder.get_iv_analysis()
print(iv_analysis)
```

## Installation

```bash
pip install fastwoe
```

For FAISS support (optional):
```bash
# CPU version
pip install fastwoe[faiss]

# GPU version
pip install fastwoe[faiss-gpu]
```

## Performance Characteristics

- **Memory Efficient**: Uses pandas and numpy for vectorized operations
- **Scalable**: Handles datasets with millions of rows
- **Fast**: Leverages sklearn's optimized TargetEncoder implementation
- **Robust**: Handles edge cases like single categories and missing values

## Use Cases

- **Credit Scoring**: Traditional scorecard development with statistical rigor
- **Risk Assessment**: Interpretable feature engineering for high-stakes decisions
- **Model Validation**: Statistical significance testing for feature selection
- **Regulatory Compliance**: Transparent models with confidence intervals

## Documentation

For detailed documentation, examples, and API reference, visit the [FastWoe GitHub repository](https://github.com/xRiskLab/fastwoe).

## License

This project is licensed under the MIT License.
