# Predictive Modeling for Agriculture

'A simple and insightful machine learning project using soil data'

## Overview

This project explores how soil characteristics can influence crop selection.
Using a small agricultural dataset with Nitrogen (N), Phosphorous (P), Potassium (K), and pH values, the goal is to understand which single soil measurement provides the strongest predictive power when recommending the most suitable crop.

The project focuses on clarity, interpretability, and practical insights rather than complex modeling — making it a great baseline analysis for real-world agricultural decision-making.

## What I Did in This Project

* Explored how each soil feature behaves (EDA)
* Visualized distributions and correlations
* Built simple Logistic Regression models, training one feature at a time
* Compared their performance to see which variable predicts crops best
* Identified the top individual soil feature for model accuracy

This is a clean, beginner-friendly machine learning workflow designed to show structured thinking and good practices — ideal for a first professional portfolio project.

## Dataset

The dataset includes four soil measurements:

* N — Nitrogen
* P — Phosphorous
* K — Potassium
* pH — Acidity/alkalinity

Each row also contains the recommended crop type for that combination of values.

## Methods Used

* Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn)
* Data cleaning and preparation
* Feature exploration & visualization
* Train/test split
* Baseline Logistic Regression models
* Single-feature model comparison

## Key Insight (Main Result)

After evaluating each soil feature individually using Logistic Regression:

**Potassium (K)** achieved the highest accuracy score among all features.
Although the model is intentionally simple, this suggests that **K levels carry meaningful predictive signal** for identifying suitable crops.

This kind of insight helps highlight which soil measurements may deserve greater attention in agricultural planning or more advanced modeling in future work.

## Why This Project Matters

* This notebook demonstrates:
* Clear structure and clean code
* Ability to build and evaluate ML baselines
* Capability to extract actionable insights (business-friendly)
* Good understanding of exploratory data analysis
* Practical communication of findings
* It is designed to be easy to read for both technical and non-technical audiences — including recruiters and hiring managers.

## Future Improvements

If expanded, the next steps could include:
* Training full multi-feature models
* Comparing multiple algorithms
* Hyperparameter tuning
* Feature importance analysis
* Building a crop recommendation system with improved accuracy
