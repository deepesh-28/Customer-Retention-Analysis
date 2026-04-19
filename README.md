# Customer-Retention-Analysis
# Customer Retention & Cohort Analysis

## Overview

This project analyzes customer retention behavior using transactional e-commerce data.
The goal is to understand how customers return over time, identify churn patterns, and quantify the revenue contribution of different customer segments.

The analysis is implemented across:

* Python (data cleaning, cohort creation)
* SQL (equivalent transformation logic)
* Tableau (interactive dashboard)

---

## Dataset

The dataset is sourced from the ** Online Retail dataset** (online retail transactions).

Due to file size limitations, the dataset is not included in this repository.
You can download it from Kaggle and place it in the `data/raw/` directory before running the notebook.

---

## Project Structure

```
Customer-Retention-Analysis/
│
├── data/
│   ├── raw/                  # Original dataset (not included)
│   └── processed/            # Cleaned data (not included)
│
├── notebooks/
│   └── Customer Retention Analysis_python.ipynb
│
├── sql/
│   └── Customer Retention Analysis_SQL.txt
│
├── dashboards/
│   └── Customer Retention Analysis.twb
│
├── images/
│   └── Customer Retention Analysis_Preview.png
│
├── README.md
└── .gitignore
```

---

## Problem Statement

* How does customer retention evolve over time?
* When does churn typically occur?
* Which customer segments drive the most revenue?
* How is churn distributed across segments?

---

## Methodology

### 1. Data Cleaning (Python)

* Removed cancelled/invalid transactions
* Handled missing `CustomerID`
* Created derived fields:

  * `Invoice Month`
  * `Cohort Month`
  * `Cohort Index`

---

### 2. Cohort Analysis

Customers are grouped based on their **first purchase month (cohort)**.

Retention is calculated as:

* Percentage of customers returning in subsequent months

This produces a **cohort retention matrix**, where:

* Rows → Cohort Month
* Columns → Months since first purchase

---

### 3. SQL Implementation

All key transformations from Python are replicated in SQL:

* Cohort creation using date functions
* Cohort index calculation
* Retention aggregation using window functions

This demonstrates cross-tool consistency in analytical logic.

---

### 4. Customer Segmentation

Customers are segmented into:

* High Value
* At Risk
* Lost
* Others

Segmentation is based on behavioral patterns derived from purchase activity.

---

### 5. Visualization (Tableau)

An interactive dashboard is built to present:

* Revenue trends over time
* Cohort retention heatmap
* Revenue contribution by segment
* Churn distribution across segments

---

## Key Insights

* Retention drops significantly after the first month
* A small proportion of customers contributes the majority of revenue (~80% range)
* Churn is concentrated among low-value and infrequent customers
* Retention stabilizes after initial drop, indicating a loyal core user base

---

## How to Use

### Python Notebook

1. Download dataset from Kaggle
2. Place in required folder in your PC
3. Download and run `Customer Retention Analysis_python` after updating the file paths for source data and output

### SQL

* Run queries from `Customer Retention Analysis_SQL.txt` in your preferred SQL environment

### Tableau

* Open `Customer Retention Analysis.twb` in Tableau Desktop

---

## Skills Demonstrated

* Cohort Analysis
* Customer Retention Metrics
* Data Cleaning & Transformation
* SQL Window Functions
* Data Visualization (Tableau)
* Business Insight Generation

---

## Notes

* Dataset is not included due to size constraints
* All analysis is reproducible using the provided code

---

## Author

Deepesh T
