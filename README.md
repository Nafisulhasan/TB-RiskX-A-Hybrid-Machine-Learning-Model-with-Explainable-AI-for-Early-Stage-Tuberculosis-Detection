# TB-RiskX: A Hybrid Machine Learning Model with Explainable AI for Early-Stage Tuberculosis Detection

TB-RiskX is a machine learning-based diagnostic framework designed for the early-stage detection of Tuberculosis (TB) using patient clinical features. To bridge the gap between complex machine learning algorithms and clinical trust, this project integrates a **Hybrid Machine Learning** architecture with **Explainable AI (XAI)** techniques (SHAP/LIME), allowing healthcare professionals to understand *why* a risk prediction was made.

## 📌 Features

* **Clinical Feature Processing:** Handles missing data, feature scaling, and class imbalance (e.g., via SMOTE) typical in medical datasets.
* **Hybrid ML Architecture:** Combines the strengths of multiple classifiers ( Tree-based ensembles like XGBoost/Random Forest combined with Logistic Regression ) to maximize sensitivity and specificity.
* **Explainable AI (XAI):** Implements global and local interpretability models to reveal feature importance and patient-specific risk factors.
* **Early-Stage Focused:** Optimized to detect TB using non-invasive clinical symptoms before advanced radiological (X-ray) or laboratory results are available.

---

## 🛠️ Tech Stack & Libraries

The analysis and model training are implemented in Python using the following core libraries:

* **Data Manipulation:** `pandas`, `numpy`
* **Machine Learning:** `scikit-learn`, `xgboost`, `lightgbm`, `catboost`
* **Explainable AI:** `shap`, `lime`
* **Visualization:** `matplotlib`, `seaborn`

---



## 🧪 Methodology & Pipeline

1. **Data Preprocessing & EDA:** - Exploration of clinical features (e.g., Cough duration, Fever, Night Sweats, Weight Loss, Age, BCG Vaccination status).
* Handling missing values and encoding categorical clinical variables.


2. **Hybrid Modeling:**
* Feature selection to extract the most predictive clinical markers.
* Training base models and combining them via a **Voting/Stacking Classifier** to build the hybrid pipeline.


3. **Evaluation:**
* Evaluated using medical-grade metrics: Accuracy, Precision, **Recall/Sensitivity** (critical for reducing false negatives in infectious diseases), F1-Score, and ROC-AUC.


4. **Explainable AI (XAI):**
* **SHAP (SHapley Additive exPlanations):** Used for global interpretability to rank clinical features by overall impact.
* **LIME (Local Interpretable Model-agnostic Explanations):** Used for case-by-case analysis to simulate how a clinician would evaluate an individual patient's risk profile.

