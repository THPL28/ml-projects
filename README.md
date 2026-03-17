# 🚢 Titanic Survival Prediction | Machine Learning

## 📌 Overview
This project applies **Machine Learning** algorithms to predict the survival probability of passengers on the RMS Titanic. Using the classic Kaggle dataset, we explore how socioeconomic and demographic variables influenced rescue outcomes.

---

## 🎯 Objective
To develop a robust predictive model capable of classifying whether a passenger survived or not, achieving a strong balance between **Precision** and **Recall**.

---

## 📊 Exploratory Data Analysis (EDA)
Before modeling, key patterns were identified in the data:
* **Gender Bias:** Female passengers had a significantly higher survival rate.
* **Class Impact:** 1st class passengers were prioritized and had better access to lifeboats.
* **Fare Correlation:** Higher fares correlate directly with survival, reflecting the socio-economic priority.

---

## 🧹 Data Engineering & Cleaning
The data preprocessing pipeline included:
* **Data Imputation:** Filled missing values in `Age` using the **Median** (more robust to outliers than the Mean).
* **Feature Selection:** Removed the `Cabin` column due to >70% missing data.
* **Categorical Encoding:** Transformed nominal variables (`Sex`, `Embarked`) into numerical format via *One-Hot Encoding*.
* **Feature Scaling:** Normalized `Fare` and `Age` to ensure model convergence.

---

## 🤖 Modeling Strategy
We utilized the **Random Forest Classifier**, an *Ensemble Learning* method, due to its resistance to overfitting and ability to handle non-linear relationships.

* **Split:** 80% Training / 20% Testing.
* **Primary Metric:** Accuracy and Confusion Matrix.
* **Cross-Validation:** Applied to ensure the stability of the results across different data folds.

---

## 📈 Results
* **Accuracy:** ~82%
* **Feature Importance:** Variables such as `Sex`, `Fare`, and `Pclass` were the primary contributors to the model's predictive power.

---

## 🧪 Deployment & Usage
Inference example for a new passenger:

```python
# Format: [Pclass, Age, Sex_Male, Fare, SibSp, Parch]
new_passenger = [[3, 22, 1, 7.25, 0, 0]]
prediction = model.predict(new_passenger)

print("Survived" if prediction[0] == 1 else "Did Not Survive")
```
## 👨‍💻 Author
Developed by **Tiago Looze** [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tiago-looze-b1a0001b7/)

