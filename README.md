# Predictive Modeling for Agriculture - Crop Recommentadation

This project explores how soil characteristics can influence crop selection.
Using a small agricultural dataset with Nitrogen (N), Phosphorous (P), Potassium (K), and pH values, the goal is to understand which individual soil measurement provides the strongest predictive power when recommending the most suitable crop.

The analysis prioritizes clarity, interpretability, and practical insights rather than complex modeling, making it a solid baseline approach for real-world agricultural decision-making.

## 1. Overview

The objective of this project is to evaluate how well a **single soil feature at a time** can predict crop types using Logistic Regression.
This helps identify which variable has the highest standalone predictive value and how soil measurements relate to crop suitability.

## 2. Dataset

The dataset includes four soil measurements:

* N — Nitrogen
* P — Phosphorous
* K — Potassium
* pH — pH level
* Crop label (target)

Each row also contains the recommended crop type for that combination of values.

## 3. Feature Exploration (EDA)

Before modeling, each soil variable was explored to understand its distribution and potential influence on crops.

Example of insights:

* Differences in nutrient ranges across crops
* How each soil measurement varies independently
* Potential separation patterns useful for prediction

## 4. Modeling Approach

Each model follows the same simple pipeline:

1. Isolate a single feature (e.g., Nitrogen only)
2. Apply train–test split
3. Train a Logistic Regression model
4. Evaluate performance on the test set
5. Compare results across all features

This structure provides a clear, interpretable baseline for understanding feature importance without introducing multivariate effects.


Key Insight (Main Result)

After evaluating each soil feature individually using Logistic Regression:

**Potassium (K)** achieved the highest accuracy score among all features.
Although the model is intentionally simple, this suggests that **K levels carry meaningful predictive signal** for identifying suitable crops.

This kind of insight helps highlight which soil measurements may deserve greater attention in agricultural planning or more advanced modeling in future work.

## Why This Project Matters

This notebook demonstrates:
* Clear structure and clean code
* Ability to build and evaluate ML baselines
* Capability to extract actionable insights (business-friendly)
* Good understanding of exploratory data analysis
* Practical communication of findings
* It is designed to be easy to read for both technical and non-technical audiences, including recruiters and hiring managers.

## Future Improvements

If expanded, the next steps could include:
* Training full multi-feature models
* Comparing multiple algorithms
* Hyperparameter tuning
* Feature importance analysis
* Building a crop recommendation system with improved accuracy
