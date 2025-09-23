---
layout: project
title: "xBooster"
description: "Scorecard framework for XGBoost and CatBoost with SQL deployment capabilities"
image: "/assets/images/projects/xbooster.png"
github: "https://github.com/xRiskLab/xBooster"
pypi: "https://pypi.org/project/xbooster/"
tags: ["Python", "XGBoost", "CatBoost", "SQL", "Machine Learning", "Deployment"]
featured: false
---

xBooster is a scorecard-format framework for logistic regression tasks with gradient-boosted decision trees (XGBoost and CatBoost). It allows you to convert a classification model into a logarithmic (point) scoring system while providing a comprehensive suite of interpretability tools.

## Key Features

- **📊 Scorecard Generation**: Convert XGBoost and CatBoost models into interpretable scorecards
- **🗄️ SQL Deployment**: Generate SQL queries for production deployment
- **🔍 Interpretability Tools**: Tree visualization, feature importance, and model explanation
- **📈 Advanced Analytics**: WOE and IV calculations, partial dependence plots
- **🎯 Production Ready**: Optimized for real-world deployment scenarios

## Interpretability Suite

- Granular boosted tree statistics, including metrics such as Weight of Evidence (WOE) and Information Value (IV) for splits 🌳
- Tree visualization with customizations 🎨
- Global and local feature importance 📊
- Score distribution analysis and model diagnostics

## Quick Start

### XGBoost Usage
```python
import pandas as pd
import xgboost as xgb
from xbooster.constructor import XGBScorecardConstructor
from sklearn.model_selection import train_test_split

# Load data and train XGBoost model
url = "https://github.com/xRiskLab/xBooster/raw/main/examples/data/credit_data.parquet"
dataset = pd.read_parquet(url)

features = [
    "external_risk_estimate",
    "revolving_utilization_of_unsecured_lines",
    "account_never_delinq_percent",
    "net_fraction_revolving_burden",
    "num_total_cc_accounts",
    "average_months_in_file",
]

target = "is_bad"
X, y = dataset[features], dataset[target]
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Train the XGBoost model
best_params = {
    'n_estimators': 100,
    'learning_rate': 0.55,
    'max_depth': 1,
    'min_child_weight': 10,
    'grow_policy': "lossguide",
    'early_stopping_rounds': 5
}
model = xgb.XGBClassifier(**best_params, random_state=62)
model.fit(X_train, y_train)

# Initialize XGBScorecardConstructor
scorecard_constructor = XGBScorecardConstructor(model, X_train, y_train)
scorecard_constructor.construct_scorecard()

# Print the scorecard
print(scorecard_constructor.scorecard)
```

### Create Scoring Points
```python
from sklearn.metrics import roc_auc_score

# Create scoring points
xgb_scorecard_with_points = scorecard_constructor.create_points(
    pdo=50, target_points=600, target_odds=50
)

# Make predictions using the scorecard
credit_scores = scorecard_constructor.predict_score(X_test)
gini = roc_auc_score(y_test, -credit_scores) * 2 - 1
print(f"Test Gini score: {gini:.2%}")
```

### Generate SQL for Deployment
```python
# Generate SQL query for production deployment
sql_query = scorecard_constructor.generate_sql_query(table_name='my_table')
print(sql_query)
```

## CatBoost Support (Beta)

xBooster provides experimental support for CatBoost models:

```python
import pandas as pd
from catboost import CatBoostClassifier, Pool
from xbooster.constructor import CatBoostScorecardConstructor

# Prepare data
data_path = "examples/data/test_data_01d9ab8b.csv"
credit_data = pd.read_csv(data_path)
num_features = ["Gross_Annual_Income", "Application_Score", "Bureau_Score"]
categorical_features = ["Time_with_Bank"]
features = num_features + categorical_features

X = credit_data[features]
y = credit_data["Final_Decision"].replace({"Accept": 1, "Decline": 0})

# Create CatBoost Pool
pool = Pool(data=X, label=y, cat_features=categorical_features)

# Initialize and train CatBoost model
model = CatBoostClassifier(
    iterations=100,
    allow_writing_files=False,
    depth=1,
    learning_rate=0.1,
    verbose=0,
    one_hot_max_size=9999,
)
model.fit(pool)

# Create and fit the scorecard constructor
constructor = CatBoostScorecardConstructor(model, pool)
scorecard = constructor.construct_scorecard()
```

## Interval Scorecards

Convert complex tree-based scorecards into simplified interval-based rules:

```python
# Build interval scorecard - simplifies complex rules into intervals
interval_scorecard = scorecard_constructor.construct_scorecard_by_intervals(add_stats=True)

print(f"Rule reduction: {len(xgb_scorecard_with_points)} → {len(interval_scorecard)} rules")

# Add Points at Even Odds/Points to Double the Odds (PEO/PDO) 
peo_pdo_scorecard = scorecard_constructor.create_points_peo_pdo(peo=600, pdo=50)
```

**Key Benefits:**
- **Simplified Rules**: Transform complex tree conditions into simple intervals like `[70.8, 80.5)`
- **Rule Reduction**: Typically 60-80% fewer rules while maintaining accuracy
- **Industry Standard**: Follows credit scoring best practices
- **Interpretable**: Easy to understand and implement in production systems

## Installation

```bash
pip install xbooster
```

## Use Cases

- **Credit Scoring**: Convert ML models into traditional scorecard format
- **Model Deployment**: Generate SQL for production systems
- **Model Validation**: Comprehensive interpretability and diagnostics
- **Regulatory Compliance**: Transparent, explainable models
- **Risk Assessment**: Interpretable scoring systems for financial institutions

## Documentation

For detailed documentation, examples, and API reference, visit the [xBooster GitHub repository](https://github.com/xRiskLab/xBooster).

## License

This project is licensed under the MIT License.
