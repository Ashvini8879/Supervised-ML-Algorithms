## 🏦 Loan Approval Predictor using Decision Tree

This project builds a machine learning model to predict whether a **loan application** should be **approved or rejected**, based on applicant details such as income, education, employment, credit history, etc.

---

### 📌 Features

* Handles missing values
* Converts categorical variables using **Label Encoding**
* Trains a **Decision Tree Classifier**
* Evaluates using **Accuracy, Precision, Recall, F1-score**
* Visualizes predictions using a **confusion matrix heatmap**

---

### 🛠️ Tools & Libraries

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib, Seaborn

---

### 📂 Dataset

**📥 Source:** [Loan Dataset - CSV](https://raw.githubusercontent.com/dphi-official/Datasets/master/Loan_Data/loan_train.csv)

```python
url = "https://raw.githubusercontent.com/dphi-official/Datasets/master/Loan_Data/loan_train.csv"
df = pd.read_csv(url)
```

---

### 🧠 ML Workflow

1. Load and explore dataset
2. Drop `Loan_ID` (not useful for prediction)
3. Handle missing values using mode/median
4. Convert categorical columns using `LabelEncoder`
5. Split data into **train/test**
6. Train a **Decision Tree Classifier**
7. Evaluate with metrics and confusion matrix

---

### 📈 Results

| Metric               | Value |
| -------------------- | ----- |
| Accuracy             | 71%   |
| Precision (Approved) | 75%   |
| Recall (Approved)    | 83%   |
| Precision (Rejected) | 59%   |
| Recall (Rejected)    | 47%   |

---

### 📊 Confusion Matrix

```
               Predicted
               0    |    1
Actual  0 →   16    |   18
        1 →   11    |   54
```

---

### ✅ Conclusion

* Model performs well at detecting **loan approvals**
* Misses some **loan rejections**, which can be improved
* Can be enhanced with:

  * **SMOTE** for balancing
  * **Random Forest**
  * **Hyperparameter tuning (GridSearchCV)**

---

### 📁 Sample Output

```python
Accuracy: 0.71

Classification Report:
              precision    recall  f1-score   support
           0       0.59      0.47      0.52        34
           1       0.75      0.83      0.79        65
```


