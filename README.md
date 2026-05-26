# MegaTelCo Churn Retention Analytics

## Predicting Customer Churn and Optimizing Retention Strategy

An end-to-end machine learning and business analytics project focused on predicting customer churn and optimizing customer retention decisions for a telecommunications company.

This project is based on the MegaTelCo churn use case from *Data Science for Business* and frames churn prediction as a business decision problem rather than only a machine learning task.

---

# Business Context

MegaTelCo, a large telecommunications provider, is experiencing substantial customer churn in its wireless business.

Approximately **20% of customers leave when their contracts expire**, creating significant revenue loss and making customer acquisition increasingly difficult.

To address this challenge, MegaTelCo's marketing team designed a **special retention offer** involving discounts and customer incentives.

However:

- The offer costs **$200 per customer**
- Budget constraints allow the company to target **only 25% of expiring customers**

Because the offer is expensive, sending it to everyone is financially impractical.

The company therefore faces a critical decision:

> Which customers should receive the retention offer in order to maximize retention and business value?

This project addresses that decision using predictive analytics and machine learning.

---

# Stakeholder Scenario

Nadia, a newly hired Data Science Product Manager at MegaTelCo, leads the churn reduction initiative.

The data science team's responsibility is to:

- Understand churn behavior
- Build predictive churn models
- Identify high-risk customers
- Recommend which customers should receive retention offers

The final objective is not simply prediction, but **actionable targeting decisions**.

---

# Business Goal

The business objective is to:

> Reduce customer churn while maximizing the return on retention spending.

Because the retention offer is expensive and limited to 25% of customers, the company must allocate resources strategically.

The project therefore focuses on:

- Increasing customer retention
- Reducing unnecessary offer spending
- Improving marketing efficiency
- Supporting data-driven decision making

---

# Data Science Problem

This is a **supervised binary classification problem**.

The predictive task is:

> Predict whether a customer will churn shortly after contract expiration.

Target variable:

- **Churn**
    - Yes
    - No

Predicted churn probabilities will then be used to prioritize customers for retention campaigns.

---

# Dataset

The project uses historical customer contract and subscription information.

## Customer Features

### Demographics

- Gender
- SeniorCitizen
- Partner
- Dependents

### Customer Relationship

- Tenure

### Phone Services

- PhoneService
- MultipleLines

### Internet and Value-Added Services

- InternetService
- OnlineSecurity
- OnlineBackup
- DeviceProtection
- TechSupport
- StreamingTV
- StreamingMovies

### Billing and Contract Information

- Contract
- PaperlessBilling
- PaymentMethod
- MonthlyCharges

### Target Variable

- Churn

---

# Key Business Questions

This project investigates several business and analytical questions.

## Churn Understanding

- Why are customers leaving?
- Which customer profiles are associated with churn?
- Are there early warning signals?

## Marketing Strategy

- Who should receive retention offers?
- Can we maximize retention while minimizing marketing cost?
- How should customers be prioritized?

## Decision Optimization

- Is predicting churn alone sufficient?
- How can prediction support operational action?

---

# Questions for Stakeholders

A successful churn project requires stakeholder clarification.

Questions for Nadia and the marketing team include:

### Retention Offer Questions

- Is the retention offer truly guaranteed to work?
- Does offer effectiveness vary by customer segment?
- Are customers eligible for multiple campaigns?

### Financial Questions

- What is customer lifetime value?
- What is the average revenue loss from churn?
- Is $200 the total cost or incremental cost?

### Operational Questions

- How frequently are targeting decisions made?
- Are there campaign execution constraints?
- What customer experience risks exist?

These questions shape model design and evaluation.

---

# Project Goals

The project aims to:

1. Predict churn probability
2. Identify churn drivers
3. Segment customer populations
4. Optimize retention targeting
5. Support business action

This project combines:

- Machine Learning
- Predictive Analytics
- Explainable AI
- Customer Intelligence
- Decision Science

---

# Project Structure

```text
megaTelco-churn-analytics/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_eda.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_modeling.ipynb
│   ├── 04_explainability.ipynb
│   ├── 05_targeting_strategy.ipynb
│   └── 06_business_recommendations.ipynb
│
├── src/
├── dashboard/
├── models/
├── reports/
├── requirements.txt
└── README.md
```

---

# Project Workflow

The project follows an end-to-end data science lifecycle.

## 1 Exploratory Data Analysis

Goals:

- Understand churn patterns
- Analyze customer behavior
- Detect anomalies
- Identify important variables

Planned analyses:

- Churn distribution
- Contract vs churn
- Tenure vs churn
- Monthly charges vs churn
- Payment method effects
- Service adoption patterns

---

## 2 Feature Engineering

Potential engineered features:

### Tenure Buckets

- 0–12 months
- 12–24 months
- 24–48 months
- 48+ months

### Service Usage Features

- Number of subscribed services
- Premium feature usage
- Internet dependency

### Risk Indicators

Potential churn signals:

- Month-to-month contracts
- Electronic check payments
- High monthly charges
- Low tenure

---

# Predictive Modeling

Multiple machine learning models will be evaluated.

| Model | Purpose |
|---|---|
| Logistic Regression | Baseline and interpretability |
| Random Forest | Nonlinear relationships |
| XGBoost | High-performance prediction |

---

# Evaluation Metrics

Churn prediction is typically imbalanced.

Evaluation includes:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

Priority metrics:

- Recall
- ROC-AUC

Missing likely churners carries substantial business cost.

---

# Explainable AI

Prediction alone is insufficient.

Business teams need to understand:

> Why is this customer predicted to churn?

This project incorporates:

## SHAP

Planned outputs:

- Global feature importance
- Individual prediction explanations
- Churn driver analysis

Expected insights:

- Contract type impact
- Pricing sensitivity
- Service usage behavior
- Customer tenure effects

---

# Retention Offer Optimization

Prediction is only part of the problem.

The marketing budget allows offers for only:

> 25% of expiring customers

The targeting strategy therefore becomes:

1. Predict churn probability
2. Rank customers by risk
3. Select top-risk customers
4. Estimate campaign impact

Decision rule:

> Offer retention incentives to customers with highest predicted churn probability subject to budget constraints.

This converts churn prediction into a **resource allocation problem**.

---

# Expected Deliverables

The data science team will produce:

## Technical Outputs

- Cleaned dataset
- Predictive models
- Evaluation results
- Explainability analysis

## Business Outputs

- Ranked customer targeting list
- Retention strategy recommendations
- Marketing decision support dashboard

These outputs support operational marketing action.

---

# Success Criteria

Success will be evaluated using both technical and business metrics.

## Model Success

- High recall
- Strong ROC-AUC
- Stable predictions

## Business Success

- Reduced churn
- Improved retention rate
- Efficient marketing spend
- Positive retention ROI

The true measure of success is:

> Lower churn achieved through better targeting decisions.

---

# Planned Dashboard

A Streamlit dashboard will enable:

- Customer-level prediction
- Churn probability display
- SHAP explanations
- Retention recommendations
- Targeting simulation

This transforms the project into an interactive business tool.

---

# Technologies

## Programming

- Python

## Data Analysis

- Pandas
- NumPy

## Visualization

- Matplotlib
- Seaborn

## Machine Learning

- Scikit-learn
- XGBoost

## Explainability

- SHAP

## Deployment

- Streamlit

## Version Control

- Git
- GitHub

---

# Future Improvements

Potential extensions:

- Retention uplift modeling
- Customer lifetime value integration
- Campaign ROI simulation
- A/B testing framework
- MLOps deployment

---

# Author

**Vrinda Tibrewal**

MS in Data Science  
New York University

Interests:

- Machine Learning
- NLP
- Product Analytics
- Decision Intelligence
- AI for Business

---

# License

MIT License
