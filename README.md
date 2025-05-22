# 🏦 Credit Card Fraud Detection: Analyzing Behavioral Patterns & Transaction Timing

**Tools:** Python | Pandas | NumPy | Scikit-learn | Statsmodels | Seaborn | Matplotlib | TextBlob

This project investigates fraudulent credit card transactions using a dataset of over 550,000 records. By combining exploratory data analysis, statistical testing, and logistic regression, we identify key predictors of fraud and provide actionable insights for financial institutions to enhance fraud detection strategies.

---

## 🔍 Methodology

- **Data Enrichment**
  - Converted transaction timestamps to datetime format
  - Calculated age from DOB
  - Created `latenight` flag (11 PM–3 AM), categorized job and age groups
- **Data Cleaning**
  - Checked for nulls and removed unnecessary rows
  - Handled class imbalance by combining all fraud cases with a 10% sample of non-fraud cases
- **Statistical Testing**
  - Chi-square and t-tests for variables like gender, time of day, day of week, and job
- **Modeling**
  - Logistic regression with key features:
    - `amt`, `latenight`, `is_high_risk_category`, `gender`, `job_category`, `age_group`, `city_pop`
  - Evaluated with:
    - AUC-ROC, Precision, Recall, F1-score

---

## 📌 Project Highlights

- **Late-night transactions (11 PM–3 AM)** strongly correlated with fraud (coeff = 2.75)
- **High-risk categories**: Online shopping, grocery, and misc. net purchases
- **Demographics**:
  - Males and legal professionals are less likely to experience fraud
  - Individuals aged 56+ are more at risk
- **Logistic Regression Results**:
  - AUC-ROC: `0.9179`
  - Precision (fraud): `84%`
  - Recall (fraud): `41%`
  - F1-score: `55%`

---

## 📁 Deliverables

- `Final Report – Credit Card.pdf`: Full technical analysis and modeling results
- Visualizations: 
  - Fraud by category and state
  - Transaction amount vs. time
  - Fraud rates by age and gender

---

## 📊 Future Improvements

- Incorporate merchant reputation and bank data
- Explore ensemble models for better fraud recall
- Test real-time classification with streaming data

---

## 📎 Dataset

Source: [Kaggle - Credit Card Fraud Prediction](https://www.kaggle.com/datasets/kelvinkelue/credit-card-fraud-prediction)

