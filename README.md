# Bundesliga Match Outcome Prediction (2019–2025)  
### CRISP-DM Applied to Time-Aware Football Modeling

This project implements a full **CRISP-DM workflow** to predict Bundesliga match outcomes using multi-season historical data (2019–20 to 2024–25).

The focus is not only on modeling performance, but on building a structured, leakage-safe, time-consistent analytical pipeline suitable for real-world football decision support.

---

## 🎯 Objective

Predict match outcomes (Home Win / Draw / Away Win) using historical Bundesliga data while:

- Preventing data leakage  
- Preserving temporal structure  
- Evaluating probability quality  
- Interpreting team-level error patterns  

---

## 🧠 Methodology: CRISP-DM Framework

### 1. Business Understanding

- Can historical performance metrics predict match outcomes?
- How stable are predictive patterns across seasons?
- What level of probability quality can realistically be achieved?

---

### 2. Data Understanding

**Data Source:**  
Football-Data.co.uk (Bundesliga CSV files)  
https://www.football-data.co.uk/germanym.php  

**Seasons covered:**

- 2019–20  
- 2020–21  
- 2021–22  
- 2022–23  
- 2023–24  
- 2024–25  

Initial steps:

- Exploratory Data Analysis (EDA)  
- Distribution analysis  
- Data quality checks  
- Missing value assessment  

---

### 3. Data Preparation

Key design decision: **Leakage-safe feature engineering**

- Rolling statistics  
- Time-aware transformations  
- No future information leakage  
- Season-consistent feature alignment  

The dataset is harmonized across multiple seasons for cross-year modeling.

---

### 4. Modeling

**Models implemented:**

- Baseline models  
- Logistic Regression  
- XGBoost  

**Validation approach:**

- GridSearchCV  
- TimeSeriesSplit (to preserve temporal order)

This ensures realistic evaluation compared to random cross-validation.

---

### 5. Evaluation

Evaluation conducted on hold-out season **2024–25**.

Metrics include:

- Accuracy  
- Class metrics  
- Probability quality  
- Calibration analysis  
- Per-team error analysis  

Special focus was placed on understanding *where* the model systematically fails, not only overall performance.

---

## 📊 Project Structure
```plaintext
CRISP-DM-FOOTBALL-ANALYTICS/
│
├── data/
│ ├── bundesliga_19-20.csv
│ ├── bundesliga_20-21.csv
│ ├── bundesliga_21-22.csv
│ ├── bundesliga_22-23.csv
│ ├── bundesliga_23-24.csv
│ └── bundesliga_24-25.csv
│
├── figures/
│ └── (model evaluation plots)
│
├── report/
│ └── CRIPS-DM_Methodology.pdf
│
├── crisp-dm_german-bundesliga-analysis.ipynb
└── README.md
```

---

## 🛠 Technical Stack

- Python  
- pandas  
- numpy  
- scikit-learn  
- XGBoost  
- matplotlib  
- Jupyter Notebook  
- Git & GitHub  

---

## 📌 Why This Project Matters

In football analytics, predictive modeling must:

- Respect temporal structure  
- Avoid leakage  
- Provide calibrated probabilities  
- Offer interpretable evaluation  

This project demonstrates how CRISP-DM can be applied to structured football outcome modeling in a professional workflow.

---

## 🔗 Author

Moritz Philipp Haaf, BSc MA

GitHub:  
https://github.com/itzmore-mph
