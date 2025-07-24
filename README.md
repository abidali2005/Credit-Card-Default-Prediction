# 🏦 Credit Card Default Prediction

This project uses a machine learning model to predict whether a customer will default on their next month’s credit card payment. It is based on the [UCI Default of Credit Card Clients Dataset](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset).

---

## 📂 Dataset Information

- **Rows**: 30,000 customers
- **Target**: `default` (1 = default, 0 = no default)
- **Features**: 23 features including credit limit, age, sex, marriage status, payment history, bill amounts, and payment amounts.

---

## 🧹 Data Preprocessing

- Removed `ID` column (identifier, not useful)
- Cleaned `EDUCATION` and `MARRIAGE` values (merged unknowns)
- No missing values in the dataset
- Scaled all numeric features using `StandardScaler`

---

## 🤖 Models Tried

| Model                   | Accuracy |
|-------------------------|----------|
| Logistic Regression     | 0.7812 ✅ (Best before tuning)  
| Support Vector Machine  | 0.7812  
| K-Nearest Neighbors     | 0.7558  
| Decision Tree           | 0.7233  
| Gaussian Naive Bayes    | 0.3817 ❌

---

## 🔍 Hyperparameter Tuning

- Tuned **Logistic Regression** using `GridSearchCV`
- Best Parameters:  
  - `C`: 1  
  - `penalty`: `'l2'`  
  - `solver`: `'liblinear'`  
- **Test Accuracy** after tuning: `~78%`

---

## 📊 Evaluation Metrics

- Accuracy
- (Optional) Precision, Recall, F1-score, ROC-AUC
- 5-fold Cross-Validation used in tuning

---

## 💡 Conclusion

The best model was **Logistic Regression** with tuned hyperparameters using `GridSearchCV`. Future work may include:
- Trying Random Forest or XGBoost
- Handling class imbalance (if present)
- ROC curve and confusion matrix visualization

---

## 📁 Tools Used

- Python
- Pandas, NumPy
- Scikit-Learn
- Matplotlib / Seaborn (for EDA)
