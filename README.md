# Credit Risk Default Analysis — Exploratory Data Analysis

## Project Overview

This project performs a structured Exploratory Data Analysis (EDA) on the UCI Credit Card Default Dataset (30,000 customers).

The objective is to identify and evaluate the primary drivers of credit card default risk through hypothesis-driven financial analysis.

The analysis focuses on behavioral repayment patterns, debt exposure, financial stability, and demographic association.

---

## Dataset Description

Source: UCI Machine Learning Repository  
Dataset: Default of Credit Card Clients (Taiwan)

The dataset contains:

- Credit limit (LIMIT_BAL)
- Repayment status for last 6 months (PAY_1 to PAY_6)
- Bill amounts (BILL_AMT1 to BILL_AMT6)
- Payment amounts (PAY_AMT1 to PAY_AMT6)
- Demographic features (SEX, EDUCATION, MARRIAGE, AGE)
- Target variable: default next month (`dpnm`)

Total observations: 30,000 customers

## Data

The dataset can be downloaded from:
UCI Machine Learning Repository:
https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients


---

## Research Questions

The analysis was structured around the following questions:

1. Is default driven by high debt levels?
2. Is default driven by repayment delays?
3. Does instability in bill or payment behavior increase risk?
4. Are demographic variables strongly associated with default?
5. Is default preceded by progressive repayment deterioration?

---

## Methodology

The analysis followed a systematic progression:

### 1. Debt Level Analysis
- Credit limit comparison
- Bill amount trends
- Absolute and relative volatility testing

### 2. Repayment Behavior Analysis
- Delay presence (>= 1 month)
- Severe delay threshold (>= 2 months)
- Recency effect (PAY_1 vs PAY_6)
- Delinquency deterioration trend

### 3. Payment Coverage Analysis
- Payment-to-bill ratio computation
- Chronic underpayment assessment

### 4. Instability Testing
- Standard deviation of bill amounts
- Relative volatility (scale-adjusted instability)

### 5. Demographic Association
- Default rate by gender
- Education-level variation
- Marital status comparison
- Age distribution analysis

---

## Key Findings

### Repayment Delinquency is the Primary Driver

- Severe delay (>= 2 months) shows strong separation between defaulters and non-defaulters.
- The most recent repayment month (PAY_1) provides the strongest signal.
- Default is preceded by progressive worsening repayment behavior.
- Delinquency intensity increases as default approaches.

### Underpayment Contributes Moderately

- Defaulters pay smaller proportions of outstanding bills on average.
- Coverage ratio is supportive but weaker than delay severity.

### Spending Instability is Not a Major Driver

- Relative bill volatility is higher among non-defaulters.
- Spending fluctuations do not strongly predict default.

### Demographic Variables Show Weak Association

- Gender differences are small.
- Education and marital status show moderate variation.
- Age shows negligible difference between groups.

---

## Conclusion

Default risk in this dataset is primarily driven by behavioral repayment deterioration rather than demographic characteristics or spending instability.

Repayment discipline, particularly delay severity and recency, is the dominant indicator of default risk.

---

## Tools and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## How to Run

```bash
git clone https://github.com/SomanMasood/credit-risk-eda.git
cd credit-risk-eda
pip install -r requirements.txt
jupyter notebook
```

---

## Future Work

- Feature engineering for predictive modeling
- Logistic regression baseline model
- Feature importance analysis
- Risk scoring framework development