# Titanic EDA — Exploratory Data Analysis & Business Insights

Exploratory data analysis on the Titanic passenger dataset, uncovering survival patterns and translating them into business insights and recommendations. Built as Project 2 in a data analytics track (Project 1 covered data cleaning).

## 📊 Overview

This project goes beyond basic cleaning to answer real business questions using the Titanic dataset:

- What factors most influenced passenger survival?
- How do class, gender, age, fare, and family size interact?
- What would a shipping company learn from this disaster to improve safety?

The analysis combines feature engineering, visual EDA, statistical testing, and a Logistic Regression model to both explore and predict survival.

## 📁 Repository Contents

| File | Description |
|---|---|
| `Titanic_EDA.ipynb` | Full analysis notebook — runs end-to-end with no errors |
| `Titanic_EDA_Report.pdf` | Polished report version of the notebook (insights + charts) |
| `Cleaned_Titanic.csv` | Cleaned dataset with engineered features |
| `Visualizations/` | All charts exported as standalone PNGs |

## 🧹 Dataset

891 passenger records with demographic info (age, sex), travel details (class, fare, cabin, port of embarkation), family relationship counts, and survival outcome. Sourced from the [Kaggle Titanic dataset](https://www.kaggle.com/competitions/titanic/data) and cleaned in a prior project — no missing values or duplicates remain.

## 🛠️ Feature Engineering

Four new features were created to enrich the analysis:

- **Family Size** — `SibSp + Parch + 1`
- **Is Alone** — Yes/No flag derived from Family Size
- **Age Group** — Child / Teenager / Adult / Senior Citizen
- **Fare Category** — Low / Medium / High Fare

## 🔍 Analysis Covered

- Data understanding (shape, types, missing values, duplicates)
- 10 business questions answered with charts and explanations (survival by gender, class, age, fare, family size, embarkation port, and more)
- Correlation heatmap
- Statistical analysis (mean, median, mode, std dev) on key numeric columns
- Summary dashboard of the six most important visualizations
- 10 business insights and 5 practical recommendations for management

## 🎁 Bonus: Logistic Regression

A Logistic Regression model predicts survival using class, sex, age, fare, family size, is-alone status, and port of embarkation.

- **Accuracy:** 80.4%
- **AUC:** 0.85
- Confusion matrix, ROC curve, and feature coefficients included

**Key takeaway:** Sex and passenger class were the dominant predictors of survival, with family structure playing a secondary role — consistent with the "women and children first" evacuation protocol and unequal lifeboat access across ticket classes.

## 🔑 Key Findings

- Only **38.4%** of passengers survived overall
- **Women survived at 74.2%** vs. **18.9%** for men
- **First class: 63.0%** survival vs. **24.2%** for third class
- **Children under 13** had the highest survival rate (58.0%) of any age group
- Small family groups (2–4 members) survived more often than solo travelers or very large families

## 🧰 Built With

- Python
- Pandas / NumPy
- Matplotlib / Seaborn
- Scikit-learn (Logistic Regression)

## ▶️ Running the Notebook

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
jupyter notebook Titanic_EDA.ipynb
```

Make sure `Cleaned_Titanic.csv` is in the same directory before running.

## 📄 License

For educational use as part of a data analytics course project.
