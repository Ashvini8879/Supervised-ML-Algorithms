# 📬 Spam Email Classifier using Logistic Regression

This project builds a Machine Learning model that classifies messages as **Spam** or **Ham (Not Spam)** using **Logistic Regression**.

---

## 📌 Features

- Preprocesses raw SMS text data
- Converts text to numerical features using **TfidfVectorizer**
- Trains a Logistic Regression model
- Evaluates using **Accuracy, Precision, Recall, and F1-score**
- Visualizes results using a **Confusion Matrix**

---

## 🛠️ Tools Used

- Python
- Pandas, NumPy
- Scikit-learn
- Seaborn, Matplotlib

---

## 📊 Dataset

We used the **SMS Spam Collection Dataset**, loaded directly from a public GitHub URL:

```python
url = "https://raw.githubusercontent.com/justmarkham/pycon-2016-tutorial/master/data/sms.tsv"
df = pd.read_csv(url, sep='\t', header=None, names=['label', 'message'])
````

### 📁 Format:

| Label | Message                        |
| ----- | ------------------------------ |
| ham   | Hey, are we meeting today?     |
| spam  | Win ₹1000000 now!!! Click here |

---

## 🧠 Machine Learning Workflow

1. Load and explore dataset
2. Preprocess and clean text data
3. Convert text to vectors using `TfidfVectorizer`
4. Split into training and test sets
5. Train a **Logistic Regression** model
6. Evaluate the model with classification metrics
7. Visualize performance using a confusion matrix

---

## 📈 Results

* **Accuracy:** \~96.68%
* **Spam Precision:** 99%
* **Spam Recall:** 78%
* **Confusion Matrix:**
  ![Confusion Matrix](https://github.com/user-attachments/assets/20626b27-fd53-4cec-96de-2ea49e74485e)

---

## ✅ Sample Output

```text
Accuracy: 0.9668

               precision    recall  f1-score   support

    ham           0.96       1.00      0.98       955
    spam          0.99       0.78      0.87       160
```

---

## 📌 Final Insight

✅ The model is **very accurate** at detecting **ham (normal messages)**.
⚠️ It **misses some spam** messages (36 out of 160) — this can be improved by trying other models like **Naive Bayes** or adding more spam training data.

---

## ▶️ How to Run

1. Clone this repository
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook: `spam_classifier.ipynb`


