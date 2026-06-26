# Heart Failure Prediction using Machine Learning

## Project Overview

This project predicts the likelihood of death in patients with heart failure using supervised machine learning algorithms. The objective is to identify the most effective classification model by comparing multiple algorithms on a clinical dataset.

The project follows a complete machine learning workflow, including:

* Exploratory Data Analysis (EDA)
* Data Preprocessing
* Feature Scaling
* Model Training
* Model Evaluation
* Hyperparameter Tuning
* Model Persistence

---

## Dataset

**Dataset:** Heart Failure Clinical Records Dataset

* Number of Patients: **299**
* Features: **12**
* Target Variable: **DEATH_EVENT**

  * **0** → Survived
  * **1** → Died

The dataset contains demographic information, laboratory measurements, and clinical parameters commonly associated with heart failure prognosis.

---

## Project Structure

```text
Heart-Failure-EDA/
│
├── data/
│   └── heart_failure_clinical_records_dataset.csv
│
├── notebooks/
│   ├── 01_EDA.ipynb
│   └── 02_Modeling.ipynb
│
├── models/
│   ├── heart_failure_rf_model.pkl
│   └── scaler.pkl
│
├── images/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Exploratory Data Analysis

The following analyses were performed:

* Dataset overview
* Missing value analysis
* Duplicate record detection
* Summary statistics
* Univariate analysis
* Bivariate analysis
* Multivariate analysis
* Correlation analysis
* Outlier detection

### Key Findings

* No missing values were present.
* No duplicate records were found.
* Creatinine phosphokinase and serum creatinine exhibited highly skewed distributions.
* Ejection fraction, serum creatinine, age, and follow-up time showed strong relationships with patient mortality.
* No severe multicollinearity was observed among predictor variables.

---

## Machine Learning Models

The following classification algorithms were evaluated:

* Logistic Regression
* Decision Tree
* Random Forest
* Support Vector Machine (SVM)
* Gradient Boosting

Hyperparameter tuning was performed using **GridSearchCV** on the Random Forest classifier.

---

## Model Performance

| Model                  |   Accuracy |    ROC-AUC |
| ---------------------- | ---------: | ---------: |
| Logistic Regression    | **81.67%** | **0.8614** |
| Decision Tree          | **75.00%** | **0.6624** |
| Random Forest          | **85.00%** | **0.8999** |
| Support Vector Machine | **76.67%** | **0.8703** |
| Gradient Boosting      | **83.33%** | **0.8447** |
| Tuned Random Forest    | **83.33%** | **0.9024** |

---

## Best Model

The **Random Forest Classifier** achieved the highest test accuracy and provided the best balance between predictive performance and generalization.

### Performance

* Accuracy: **85.00%**
* ROC-AUC: **0.8999**

The tuned Random Forest achieved a slightly higher ROC-AUC (**0.9024**) during testing but did not improve overall accuracy.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib
* Jupyter Notebook

---

## Installation

Clone the repository:

```bash
git clone https://github.com/<your-username>/Heart-Failure-EDA.git
```

Install the required packages:

```bash
pip install -r requirements.txt
```

---

## Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Run the notebooks in the following order:

1. `01_EDA.ipynb`
2. `02_Modeling.ipynb`

---

## Results

The Random Forest classifier demonstrated the strongest predictive performance, outperforming the other evaluated models in terms of accuracy while maintaining excellent discrimination capability.

Important predictors included:

* Time
* Ejection Fraction
* Serum Creatinine
* Age

These findings are consistent with established clinical knowledge regarding heart failure prognosis.

---

## Future Improvements

* Evaluate XGBoost and LightGBM
* Address class imbalance using SMOTE
* Perform nested cross-validation
* Deploy the model using Streamlit or Flask
* Integrate SHAP for model explainability

---

## Author

**Vani Goel**

B.Tech Electronics and Communication Engineering (Biomedical Engineering)

VIT Vellore
