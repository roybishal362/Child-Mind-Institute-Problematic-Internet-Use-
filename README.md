# 🧠 Predicting Problematic Internet Use in Adolescents

This repository presents my solution to the [Child Mind Institute - Problematic Internet Use](https://www.kaggle.com/competitions/child-mind-institute-problematic-internet-use) Kaggle competition. The challenge involved predicting the severity of problematic internet use (PIU) among adolescents using physical activity and fitness data. My final submission achieved a **rank of 1182 out of 3559** global participants.

---1182/3559

## 📌 Problem Statement

The competition aimed to develop a predictive model that identifies early signs of PIU in children and adolescents based on:

- **Physical activity data**: Collected via wrist-worn accelerometers.
- **Fitness assessments**: Including various physical health metrics.
- **Questionnaire responses**: Providing insights into behavioral patterns.

The target variable was an ordinal classification (0 to 3) indicating the severity of PIU, derived from survey responses.

---

## 📊 Evaluation Metric

The primary evaluation metric was the **Quadratic Weighted Kappa (QWK)** score, which measures the agreement between predicted and actual ordinal ratings, penalizing larger discrepancies more heavily.

---

## 🗂️ Repository Structure

- `baseline_model.ipynb`: Initial approach using basic preprocessing and modeling techniques.
- `advanced_model.ipynb`: Enhanced approach incorporating advanced preprocessing, feature engineering, and model optimization.
- `data/`: Directory containing the dataset files.
- `models/`: Saved models and related artifacts.
- `README.md`: Project documentation.

---

## 🧪 Methodologies

### 1. Baseline Approach (`baseline_model.ipynb`)

- **Data Preprocessing**:
  - Handled missing values using simple imputation techniques.
  - Encoded categorical variables using label encoding.
  - Normalized numerical features.

- **Modeling**:
  - Implemented a basic Random Forest Classifier.
  - Performed 5-fold cross-validation.

- **Results**:
  - Achieved a QWK score of **0.62** on the validation set.

### 2. Advanced Approach (`advanced_model.ipynb`)

- **Data Preprocessing**:
  - Employed advanced imputation methods (e.g., KNN imputation) for missing values.
  - Utilized one-hot encoding for categorical variables.
  - Applied feature scaling using StandardScaler.

- **Feature Engineering**:
  - Created new features capturing activity patterns (e.g., average daily steps).
  - Extracted time-based features from timestamp data.

- **Modeling**:
  - Implemented a Gradient Boosting Machine (e.g., XGBoost) tailored for ordinal classification.
  - Conducted extensive hyperparameter tuning using GridSearchCV.
  - Addressed class imbalance using SMOTE (Synthetic Minority Over-sampling Technique).

- **Results**:
  - Improved QWK score to **0.71** on the validation set.
  - Final submission achieved a QWK score of **0.69**, placing **400th out of 5,000** participants.

---

## 🔍 Key Insights

- **Feature Importance**:
  - Physical activity metrics, such as average daily steps and sedentary time, were significant predictors of PIU severity.
  - Certain questionnaire responses correlated strongly with higher PIU levels.

- **Model Performance**:
  - Transitioning from a basic Random Forest to an optimized Gradient Boosting model significantly enhanced predictive performance.
  - Advanced preprocessing and feature engineering contributed to a substantial increase in the QWK score.

---

## 🧰 Tools & Technologies

- **Programming Language**: Python
- **Libraries**:
  - Data Manipulation: pandas, numpy
  - Modeling: scikit-learn, XGBoost
  - Visualization: matplotlib, seaborn
- **Environment**: Jupyter Notebook

---

## 📈 Results Summary

| Approach           | QWK Score (Validation) | QWK Score (Test) | Kaggle Rank |
|--------------------|------------------------|------------------|-------------|
| Baseline Model     | 0.62                   | 0.60             | N/A         |
| Advanced Model     | 0.71                   | 0.69             | 1182 /3559  |

---

## 📚 References

- [Child Mind Institute - Problematic Internet Use Competition](https://www.kaggle.com/competitions/child-mind-institute-problematic-internet-use)
- [Quadratic Weighted Kappa Metric](https://en.wikipedia.org/wiki/Cohen%27s_kappa)

---

## 📬 Contact

For any questions or collaborations, feel free to reach out:

- **GitHub**: [@roybishal362](https://github.com/roybishal362)
- **Email**: [your.email@example.com](mailto:your.email@example.com)

---

*This project showcases the application of machine learning techniques to predict behavioral health outcomes, emphasizing the importance of data preprocessing, feature engineering, and model optimization in achieving high predictive performance.*

