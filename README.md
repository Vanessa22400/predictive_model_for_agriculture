# Predictive Modeling for Agriculture - Crop Recommentadation

This project explores how soil characteristics can influence crop selection.
Using a small agricultural dataset with Nitrogen (N), Phosphorous (P), Potassium (K), and pH values, the goal is to understand which individual soil measurement provides the strongest predictive power when recommending the most suitable crop.

The analysis prioritizes clarity, interpretability, and practical insights rather than complex modeling, making it a solid baseline approach for real-world agricultural decision-making.

---

### 1. Project Overview

The objective is to train **four Logistic Regression models**, each using only one soil feature at a time.
This approach helps answer a simple but important question:

**“Which individual soil variable best predicts crop type?”**

This provides a transparent understanding of feature importance and sets the foundation for more advanced modeling later.

---

### 2. Dataset

The dataset used is `soil_measures.csv`, containing four soil features and a target label indicating the recommended crop:

* **N**: Nitrogen level
* **P**: Phosphorous level
* **K**: Potassium level
* **ph**: pH level
* **crop** (target): Recommended crop for that soil sample

---

### 3. Modeling Approach

To keep the analysis simple and interpretable, each soil feature is tested independently.

For each feature (N, P, K, pH):

1. A **train-test** split is performed.
2. A **Logistic Regression** model is trained using only that variable.
3. Model accuracy is recorded.

This method reveals which single soil measurement provides the strongest predictive signal for crop classification.

---

### 4. Results

Each Logistic Regression model was trained using only one soil feature at a time.
The accuracy scores were:

* **Nitrogen (N):** 0.143
* **Phosphorous (P):** 0.189
* **Potassium (K):** 0.248
* **pH:** 0.098

#### Key Insight 

After evaluating each soil feature individually using Logistic Regression:

**Potassium (K)** achieved the highest accuracy score among all features.
Even though the models are intentionally simple, this indicates that **K levels provide the strongest individual predictive signal** for identifying suitable crops.

This insight suggests that potassium may deserve greater attention in agricultural analysis and could be particularly valuable in a more complete multi-feature or advanced modeling workflow.

### 5. Future Improvements

If expanded, the next steps could include:
* Training full multi-feature models
* Comparing multiple algorithms
* Hyperparameter tuning
* Feature importance analysis
* Building a crop recommendation system with improved accuracy
