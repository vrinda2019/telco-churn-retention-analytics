# Telco Churn Retention Analytics

## Predicting Customer Churn and Designing Data-Driven Retention Strategies

An end-to-end machine learning and analytics project focused on predicting customer churn in the telecommunications industry and identifying actionable customer retention strategies using interpretable machine learning.

---

## Project Overview

Customer churn is one of the most critical business challenges for subscription-based companies. Acquiring new customers is often significantly more expensive than retaining existing ones.

This project aims to:

- Predict which customers are likely to churn
- Understand the behavioral and financial drivers of churn
- Identify high-risk customer segments
- Provide interpretable business insights
- Recommend retention strategies based on data

Rather than treating churn prediction as only a machine learning problem, this project approaches it as a business decision-making problem.

---

## Business Problem

Telecommunication companies face significant revenue loss due to customer churn.

The key business questions addressed are:

1. Which customers are most likely to churn?
2. What factors contribute to churn?
3. Can churn risk be predicted early?
4. Which customer groups require targeted retention strategies?
5. How can analytics support business intervention decisions?

---

## Dataset

### IBM Telco Customer Churn Dataset

The dataset contains customer-level information for a telecom provider.

Features include:

### Customer Information

- Gender
- Senior citizen status
- Partner
- Dependents

### Subscription Services

- Phone service
- Multiple lines
- Internet service
- Online security
- Online backup
- Device protection
- Tech support
- Streaming TV
- Streaming movies

### Account Information

- Tenure
- Contract type
- Paperless billing
- Payment method
- Monthly charges
- Total charges

### Target Variable

- **Churn**
    - Yes
    - No

---

## Project Goals

This project combines:

- Predictive analytics
- Machine learning
- Customer segmentation
- Explainable AI
- Business intelligence

The objective is not only to build accurate models but also to generate actionable insights.

---

## Project Structure

```text
telco-churn-retention-analytics/
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
│   └── 05_business_recommendations.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── features.py
│   ├── train.py
│   └── evaluate.py
│
├── dashboard/
│
├── models/
│
├── reports/
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Project Workflow

The project follows an end-to-end data science pipeline.

### 1. Exploratory Data Analysis (EDA)

Objectives:

- Understand customer behavior
- Analyze churn distribution
- Detect trends and patterns
- Identify missing values and anomalies

Planned analyses:

- Churn distribution
- Contract type vs churn
- Tenure vs churn
- Monthly charges vs churn
- Service adoption patterns
- Correlation analysis

---

### 2. Feature Engineering

Additional features may include:

### Tenure Groups

Customer lifecycle buckets:

- 0–12 months
- 12–24 months
- 24–48 months
- 48+ months

### Service Usage Features

Examples:

- Number of subscribed services
- Internet dependency indicators
- Premium service indicators

### Risk Indicators

Potential churn-related signals:

- Month-to-month contracts
- Electronic check payments
- High monthly charges
- Low tenure

---

### 3. Predictive Modeling

Multiple machine learning models will be evaluated.

Planned models:

| Model | Purpose |
|---|---|
| Logistic Regression | Interpretable baseline |
| Random Forest | Nonlinear relationships |
| XGBoost | High-performance tabular modeling |

---

## Evaluation Metrics

Because churn prediction is often an imbalanced classification problem, evaluation extends beyond accuracy.

Metrics:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

Special focus:

- Recall
- ROC-AUC

These metrics better capture the business cost of missing churn-prone customers.

---

## Explainable AI (XAI)

Model interpretability is critical for business adoption.

This project incorporates:

### SHAP (SHapley Additive Explanations)

Objectives:

- Explain individual predictions
- Identify global feature importance
- Understand churn drivers

Planned visualizations:

- SHAP summary plots
- Feature importance rankings
- Local prediction explanations

This enables decision-makers to understand *why* customers are predicted to churn.

---

## Customer Segmentation

Beyond prediction, this project explores customer segmentation.

Potential clustering techniques:

- K-Means clustering

Possible customer segments:

- Loyal customers
- High-value subscribers
- Price-sensitive users
- High-risk churn customers

Segmentation helps design targeted retention campaigns.

---

## Business Recommendations

The final stage focuses on business impact.

Potential outputs:

| Customer Segment | Churn Risk | Recommended Action |
|---|---|---|
| New Customers | High | Onboarding support |
| High-Value Customers | Medium | Loyalty rewards |
| Contract-Free Customers | High | Contract incentives |

The goal is to bridge machine learning outputs with operational decisions.

---

## Interactive Dashboard

Planned deployment:

### Streamlit Dashboard

Features:

- Customer input form
- Real-time churn prediction
- Churn probability score
- Explainability insights
- Business recommendations

This transforms the project from analysis into a usable application.

---

## Technologies Used

### Programming

- Python

### Data Analysis

- Pandas
- NumPy

### Visualization

- Matplotlib
- Seaborn

### Machine Learning

- Scikit-learn
- XGBoost

### Explainability

- SHAP

### Deployment

- Streamlit

### Version Control

- Git
- GitHub

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/telco-churn-retention-analytics.git
```

Move into project folder:

```bash
cd telco-churn-retention-analytics
```

Create virtual environment:

### Mac/Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the Project

Launch Jupyter:

```bash
jupyter notebook
```

Run notebooks in sequence:

1. EDA
2. Feature Engineering
3. Modeling
4. Explainability
5. Business Insights

---

## Future Improvements

Potential extensions:

- A/B testing for retention campaigns
- Retention intervention simulation
- Model monitoring pipeline
- Cloud deployment
- MLOps integration
- Advanced uplift modeling

---

## Expected Outcomes

This project aims to demonstrate:

- End-to-end machine learning workflow
- Applied business analytics
- Explainable AI
- Customer intelligence
- Product and retention analytics

---

## Author

**Vrinda Tibrewal**

MS Data Science — New York University

Interested in:

- Data Science
- Machine Learning
- NLP
- Product Analytics
- AI-driven decision systems

---

## License

MIT License
