# Data Analytics Portfolio

A collection of end-to-end analytics projects built around real business problems in sales, marketing, and customer intelligence. Each project covers the full workflow — data cleaning, exploratory analysis, modeling or statistical testing, and actionable business recommendations — using Python and industry-standard tools.

---

## Project Overview

| # | Project | Domain | Key Skills | Status |
|---|---------|--------|------------|--------|
| 1 | [Sales Performance Dashboard](#-project-1-sales-performance-dashboard) | Revenue Analytics | Pandas, Plotly, Streamlit | Complete |
| 2 | [Customer Churn Prediction](#-project-2-customer-churn-prediction) | Customer Retention | Classification, Scikit-learn, XGBoost | Planned |
| 3 | [Lead Scoring Model](#-project-3-lead-scoring-model) | Sales Ops | Logistic Regression, Feature Engineering | Planned |
| 4 | [Sales Forecasting](#-project-4-sales-forecasting) | Revenue Planning | Prophet, Time Series, Statsmodels | Planned |
| 5 | [Funnel Drop-off Analysis](#-project-5-funnel-drop-off-analysis) | Marketing Analytics | CRM Analysis, Cohort Analysis, Plotly | Planned |
| 6 | [A/B Test Analysis](#-project-6-ab-test-analysis) | Experimentation | Hypothesis Testing, SciPy, Statistics | Planned |
| 7 | [Competitive Price Scraper](#-project-7-competitive-price-scraper) | Market Intelligence | Web Scraping, BeautifulSoup, Selenium | Planned |

---

## 📊 Project 1: Sales Performance Dashboard

**Business question:** Which reps, products, and regions are driving revenue — and where are the opportunities?

[View Repository](https://github.com/jsusacortes/Sales-performance-dashboard.git)

### Business Context
A chocolate sales company needs visibility into rep performance, product margins, and regional trends to make informed decisions about where to coach, invest, and expand. This interactive dashboard replaces static reports with a filterable, real-time view of the business.

### Dataset
- Chocolate sales transactions including rep name, country, product, date, revenue, and boxes shipped

### Approach
1. **Data Cleaning:** Standardized date formats, handled missing values, engineered revenue-per-box metric
2. **EDA:** Identified seasonal trends, rep performance clusters, and product margin profiles
3. **Dashboard:** Multi-page Streamlit app with dynamic filters by country, rep, and date range

### Key Insights
- Revenue peaked in January ($896K), dipped mid-year, then recovered to $865K in June — indicating a recurring seasonal pattern
- Top 5 reps are tightly clustered ($311K–$321K); Rafaelita Blaksland leads in deal quality at $48.93/box despite mid-table revenue — she targets premium accounts
- Karlen McCaffrey ships the most boxes (9,658) at the lowest $/box ($23.18) — a coaching opportunity to shift toward higher-margin products
- Peanut Butter Cubes is the most balanced product: high volume with strong margins

### Skills Demonstrated
- Data cleaning and feature engineering with **pandas**
- Interactive visualizations with **Plotly Express**
- Multi-page dashboard with dynamic filters using **Streamlit**
- EDA structured around business questions, not just statistics

---

## 🔄 Project 2: Customer Churn Prediction

**Business question:** Which customers are likely to cancel — and what can we do before they leave?

[View Repository](#)

### Business Context
Retaining an existing customer costs far less than acquiring a new one. By identifying high-risk accounts before they churn, customer success teams can intervene with targeted outreach and reduce revenue loss.

### Approach
1. Exploratory analysis of customer behavior, contract type, and service usage patterns
2. Feature engineering: tenure buckets, service count, monthly vs. total charge ratio
3. Modeling: Logistic Regression baseline → Random Forest → XGBoost with hyperparameter tuning
4. Evaluation focused on **recall** (minimize missed churners) with precision-recall tradeoff analysis
5. Feature importance analysis to surface the most actionable churn drivers

### Skills Demonstrated
- Binary classification with **scikit-learn** and **XGBoost**
- Handling class imbalance (SMOTE / class weighting)
- Business-driven model evaluation (recall over accuracy)
- Churn driver interpretation for non-technical stakeholders

---

## 🎯 Project 3: Lead Scoring Model

**Business question:** Which leads should sales prioritize to maximize conversion rate?

[View Repository](#)

### Business Context
Sales teams waste time on low-intent leads when high-intent prospects go uncontacted. A data-driven lead scoring model ranks incoming leads by conversion probability, letting reps focus effort where it counts.

### Approach
1. Analysis of lead source, engagement behavior, and demographic signals
2. Feature engineering: channel interactions, engagement score composites
3. Modeling: Logistic Regression → Decision Tree → Random Forest with cross-validation
4. Output: ranked lead scores deployable as a CRM integration or CSV export

### Skills Demonstrated
- End-to-end classification pipeline with **scikit-learn**
- Feature selection and multicollinearity analysis
- Model interpretability with SHAP values
- Translating model output into a prioritized lead queue

---

## 📈 Project 4: Sales Forecasting

**Business question:** What will revenue look like over the next 90 days?

[View Repository](#)

### Business Context
Accurate revenue forecasts allow finance and sales leadership to set realistic targets, plan headcount, and manage inventory. This project builds a time series model trained on historical sales data to generate forward-looking projections with confidence intervals.

### Approach
1. Time series decomposition: trend, seasonality, and residual analysis
2. Stationarity testing (ADF test) and differencing where needed
3. Modeling: Prophet baseline → SARIMA → comparison against a simple rolling average
4. Forecast evaluation: MAE, RMSE, and MAPE on a held-out test window

### Skills Demonstrated
- Time series analysis with **Prophet** and **statsmodels**
- Seasonality decomposition and stationarity testing
- Forecast visualization with confidence intervals using **Plotly**
- Communicating uncertainty in projections to business stakeholders

---

## 🔍 Project 5: Funnel Drop-off Analysis

**Business question:** Where in the sales funnel are we losing the most prospects — and why?

[View Repository](#)

### Business Context
CRM data captures every stage of the sales process, but few teams systematically analyze where and why deals stall. This project maps the full funnel, quantifies stage-level conversion rates, and identifies the deal characteristics associated with drop-off.

### Approach
1. Funnel construction from raw CRM stage data (lead → MQL → SQL → opportunity → closed won)
2. Cohort analysis: conversion rates by rep, source, industry, and deal size
3. Statistical comparison of won vs. lost deals at each stage
4. Visualization: Plotly funnel charts and heatmaps for stakeholder presentation

### Skills Demonstrated
- CRM data wrangling and funnel construction with **pandas**
- Cohort and segment analysis
- Funnel and heatmap visualizations with **Plotly**
- Turning drop-off data into prioritized process recommendations

---

## 🧪 Project 6: A/B Test Analysis

**Business question:** Did the new email subject line / landing page / pricing tier actually perform better?

[View Repository](#)

### Business Context
Marketing and product teams run experiments constantly but often draw conclusions from raw conversion rates without accounting for statistical significance, sample size, or test duration. This project applies rigorous hypothesis testing to evaluate experiment results.

### Approach
1. Experiment design review: sample size calculation, power analysis, randomization checks
2. Statistical testing: two-proportion z-test, chi-square test for independence
3. Bayesian A/B analysis as an alternative to p-values for business audiences
4. Sensitivity analysis: how long must the test run to detect a meaningful effect?

### Skills Demonstrated
- Hypothesis testing with **SciPy**
- Sample size and power calculations
- Bayesian inference for experimentation
- Clear communication of statistical results to non-technical decision-makers

---

## 🕷️ Project 7: Competitive Price Scraper

**Business question:** How does our pricing compare to competitors — and is it changing?

[View Repository](#)

### Business Context
Pricing teams need real-time competitive intelligence to stay positioned correctly in the market. Manual price checks don't scale. This project automates the collection, storage, and comparison of competitor pricing data across multiple product categories.

### Approach
1. Web scraping with **BeautifulSoup** for static pages and **Selenium** for JavaScript-rendered content
2. Data pipeline: scrape → clean → store → compare against internal pricing
3. Price change detection: alerts when a competitor moves by more than a defined threshold
4. Visualization: side-by-side price comparison dashboard

### Skills Demonstrated
- Web scraping with **requests**, **BeautifulSoup**, and **Selenium**
- Building a repeatable data pipeline
- Price change detection and alerting logic
- Ethical scraping practices (rate limiting, robots.txt compliance)

---

## How to Run

Each project is self-contained. General setup:

```bash
# Create and activate a virtual environment
python -m venv venv
source venv/Scripts/activate  # Windows (Git Bash)

# Install project dependencies
pip install -r <project-folder>/requirements.txt

# Streamlit dashboards
streamlit run <project-folder>/app.py

# Jupyter notebooks
jupyter notebook <project-folder>/

# Python scripts
python <project-folder>/main.py
```

All notebooks are also compatible with **Google Colab** — no local setup required.

---

## Tech Stack

| Category | Tools |
|----------|-------|
| Data manipulation | pandas, numpy |
| Visualization | Plotly, Matplotlib, Seaborn |
| Dashboards | Streamlit |
| Machine learning | Scikit-learn, XGBoost |
| Time series | Prophet, Statsmodels |
| Statistical testing | SciPy |
| Web scraping | Requests, BeautifulSoup, Selenium |

---

## Author

**Juan Susa**
[LinkedIn](https://www.linkedin.com/in/juan-camilo-susa-cortes-380186262)

*This portfolio demonstrates applied data analytics skills across the full project lifecycle: business framing, data wrangling, analysis, modeling, and stakeholder-ready communication of findings.*
