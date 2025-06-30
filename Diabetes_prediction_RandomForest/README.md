# 🩺 Diabetes Prediction using Random Forest Classifier

This project is part of my **Supervised Machine Learning Series** where I build models using real-world datasets. This one predicts whether a person is likely to have diabetes using Random Forest.

---

## 📂 Dataset

📥 Dataset is loaded from the following URL:

```python
url = "https://raw.githubusercontent.com/plotly/datasets/master/diabetes.csv"
````

This includes 768 patient records with the following features:

* Pregnancies, Glucose, BloodPressure, SkinThickness, Insulin, BMI, DiabetesPedigreeFunction, Age
* Outcome: 1 (Diabetic), 0 (Not Diabetic)

---

## ✅ Steps Performed

| Step | Description                                                           |
| ---- | --------------------------------------------------------------------- |
| 1️⃣  | Loaded the dataset using pandas from URL                              |
| 2️⃣  | Checked for null values (no missing data)                             |
| 3️⃣  | Split data into features (`X`) and labels (`y`)                       |
| 4️⃣  | Used `train_test_split()` to create 80% training and 20% testing data |
| 5️⃣  | Trained a `RandomForestClassifier` with 100 trees                     |
| 6️⃣  | Predicted results and evaluated model                                 |
| 7️⃣  | Plotted a Confusion Matrix and printed Classification Report          |

---

## 🔧 Libraries Used

* pandas, numpy
* scikit-learn (`RandomForestClassifier`, `accuracy_score`, `classification_report`, `confusion_matrix`)
* seaborn, matplotlib (for heatmap visualization)

---

## 📈 Sample Output

### 🔹 Accuracy

```
Accuracy: 0.75
```

### 🔹 Classification Report

| Label           | Precision | Recall | F1-Score | Support |
| --------------- | --------- | ------ | -------- | ------- |
| 0 (No Diabetes) | 0.81      | 0.79   | 0.80     | 99      |
| 1 (Diabetic)    | 0.64      | 0.67   | 0.65     | 55      |

### 🔹 Confusion Matrix

|           | Predicted: 0 | Predicted: 1 |
| --------- | ------------ | ------------ |
| Actual: 0 | ✅ 78 (TN)    | ❌ 21 (FP)    |
| Actual: 1 | ❌ 18 (FN)    | ✅ 37 (TP)    |

---

## 🧠 Conclusion

* 🔸 Model is strong at predicting **non-diabetic (class 0)** cases
* 🔸 Struggles a bit on predicting **diabetic (class 1)** patients
* ⚠️ Might falsely mark some diabetic patients as non-diabetic (high risk in real life)
* Can be improved by:

  * Balancing dataset (SMOTE)
  * Tuning RandomForest hyperparameters
  * Trying other classifiers like XGBoost or SVM

---

## 🧪 Folder Content

> This project is stored under the folder:

```
Supervised-ML-Algorithms/
└── Diabetes_prediction_RandomForest/
    └── Diabetes_prediction_RandomForest.ipynb
```

🗂️ *Prediction outputs and saved models are excluded from repo to keep it clean.*

---

## 🙋‍♂️ Author

**Ashu Davale**
MCA Student | Python & ML Enthusiast

---

