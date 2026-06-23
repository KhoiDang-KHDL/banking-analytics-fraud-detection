# 🏦 Banking Analytics Fraud Detection 🛡️

**Notebook:** `banking_transaction.ipynb`  
**Dashboard Export:** `Dashboard.pbix`  
**Author:** `Nguyễn Đăng Khôi`  
**Project Type:** Power BI + Python  

---

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=flat"/>
</p>

---

## 🔍 Project Overview & Objectives

Fraud detection and customer lifetime value optimization are core challenges in the banking and financial sectors. This project tackles advanced customer behavioral analytics integrated with anomaly detection using transactional bank data based on two main pillars:
1. **Business Optimization:** Behavioral customer segmentation (RFM Analysis), customer lifetime value modeling (CLV), growth rate measurement (QoQ), and cohort retention analysis.
2. **Risk Management:** Deploying unsupervised machine learning algorithms to detect potential ror-risk behaviors and anomalous transactions without relying on predefined labels.

The entire analytical workflow is consolidated into an **Interactive Power BI Dashboard** designed for risk managers and business operators to drive data-backed strategic decisions.

---

## 💡 Key Insights & Business Recommendations

| Analytics Dimension | Key Finding & Insight | Business Recommendation |
|---|---|---|
| **Fraud Risk (Isolation Forest)** | Fraudulent transactions exhibit extremely high **Amount** and **Fees**, heavily concentrated in `Loan Payment` activities under the `Loan` and `Credit Card` product categories. | **Tighten automated auditing controls** for loan settlements with abnormally large values; implement real-time Multi-Factor Authentication (MFA) for transactions exceeding safety thresholds. |
| **Fraud Risk (Local Outlier Factor)** | Detects more sophisticated anomalies at a local density level. High anomaly scores correlate with customers having **Low Income** in the Low and Middle segments. | **Closely monitor cash flows** for accounts showing high financial distress to prevent account mule activities or fraudulent credit line applications. |
| **Customer Segmentation (RFM)** | Applying the Pareto Principle (80/20 rule), a major portion of total revenue and fee income is contributed by VIP customer segments (`Champions` and `Loyal Customers`). | **Design exclusive loyalty programs** tailored to retain high-value segments; launch automated re-engagement marketing campaigns for the `At Risk` group. |
| **Retention & Value (CLV & Cohort)** | Customer retention rates drop significantly over consecutive months; customer lifetime value (CLV) shows deep polarization between High-Income customers and other segments. | **Optimize the onboarding experience** within the first 3 months of the customer lifecycle (where Churn peaks) and personalize `Recommended Offer` catalogs based on segment financial profiles. |

---

## 🔄 End-to-End Pipeline
```text
1. Business Understanding    Define goals: Maximize Customer Value & Detect Fraud Risk
         ↓
2. Data Preprocessing        Data cleaning, missing value handling, normalization, Feature Engineering
         ↓
3. Behavioral Analytics      Implement RFM Segmentation, Cohort Matrix, QoQ Growth & CLV
         ↓
4. Anomaly Detection         Unsupervised ML Modeling: Isolation Forest & Local Outlier Factor
         ↓
5. Dimensionality Reduction  Apply PCA (2D Projection) to visualize anomaly separation boundaries
         ↓
6. BI Implementation         Develop a multi-tier governance interactive dashboard on Power BI
---

## 📊 Power BI Dashboard Architecture

The dashboard is structured into clear analytical views, catering to both high-level executive overviews and deep-dive technical tracking:

### 1. Financial & Business Campaign Overview
*Provides a bird's-eye view of overall financial health and operational performance metrics.*
* **Core Metrics:** Total transaction volume, transaction frequency, total capital flow (`Total Amount`), average monthly income (`Monthly Income`), and credit rating (`Customer Score`).
* **Visualizations:** Monthly cash flow trends, transaction type distribution (`Transaction Type`), and capital flow share by channel (`Channel`).
* *Dashboard Preview:*
<p align="center">
  <img src="Images/Overview.png" width="900" alt="Overview Dashboard"/>
</p>

### 2. Customer Insights Analysis
*Delves deep into customer demographics, financial behaviors, and financial product adoption.*
* **Visualizations:** Correlation between credit scores and transactional behavior; financial product market share by income segment and profession.
* *Dashboard Preview:*
<p align="center">
  <img src="Images/CustomerAnalysis.png" width="900" alt="Customer Analysis Dashboard"/>
</p>

### 3. Revenue & Customer Behavior
*Deconstructs fee revenue streams and analyzes recommended offer conversions to optimize profitability.*
* **Visualizations:** Fee breakdown analysis (`Credit Card Fees`, `Insurance Fees`, `Late Payment Amount`); revenue driven by personalized product marketing campaigns (`Recommended Offer`).
* *Dashboard Preview:*
<p align="center">
  <img src="Images/Revenue_&_Customer.png" width="900" alt="Revenue Analysis Dashboard"/>
</p>

### 4. Advanced Customer Analysis (RFM, Cohort & Retention)
*Advanced customer behavioral intelligence layer to optimize long-term user retention strategies.*
* **Visualizations:** RFM behavioral segmentation customer distribution grid (`Advanced_Analysis.png`, `RFM.png`); Cohort Analysis heat map measuring progressive Retention Rate over months (`Cohort.png`, `Retention_Rate.png`); Quarter-over-Quarter growth charts (`QoQ.png`); and Customer Lifetime Value forecasting distribution (`Customer_Lifetime.png`)[cite: 3].
* *Dashboard Preview:*
<p align="center">
  <img src="Images/RFM.png" width="900" alt="RFM Analysis Dashboard"/>
</p>
<p align="center">
  <img src="Images/Cohort.png" width="900" alt="Cohort Analysis Dashboard"/>
</p>

### 5. AI-Powered Anomaly & Fraud Detection
*Risk monitoring layer leveraging Machine Learning models to intercept suspicious activities early.*
* **Visualizations:** Anomaly vs. Normal boundaries mapped via Principal Component Analysis (2D PCA Projection); Anomaly Score density distribution; Comprehensive behavioral profiling table for high-risk accounts flagged by models.
* *Dashboard Preview:*
<p align="center">
  <img src="Images/Anomalies.png" width="900" alt="Anomaly Detection Dashboard"/>
</p>

---

## 🛠️ Skills & Technologies Demonstrated

| Domain | Technical Implementation |
|---|---|
| **Data Engineering** | Processing large-scale relational data (20,000+ records), missing value imputation, transaction timestamp standardization, and data type alignment. |
| **Advanced Analytics** | Engineering behavior indicators: Recency, Frequency, Monetary metrics; modeling long-term CLV and creating progressive customer retention matrices (Cohort Matrix). |
| **Unsupervised ML** | Deploying Isolation Forest (global outlier detection) and Local Outlier Factor (localized density anomaly detection); applying PCA dimensionality reduction to visualize multi-dimensional data partitions. |
| **Business Intelligence** | Designing corporate-grade relational Power BI schemas, establishing robust star-schema data models, and optimizing advanced DAX expressions for complex time-intelligence metrics (Cohort, CLV, QoQ). |

---

## 📁 Project Structure

```text
banking-analytics-fraud-detection/
├── Code/
│   └── banking_transaction.ipynb    # Full Jupyter Notebook source code (EDA, Preprocessing, ML Models)
├── Data/                            # Project data repository
│   ├── Banking_Transactional_Dataset.csv # Raw bank transaction dataset
│   ├── RankRFM.csv                       # Computed RFM customer segment metadata
│   └── isolation_output.csv              # Transaction records with anomaly flags appended by ML models
├── Images/                          # Dashboard screenshots for repository presentation
│   ├── Overview.png
│   ├── CustomerAnalysis.png
│   ├── Revenue_&_Customer.png
│   ├── RFM.png
│   ├── Cohort.png
│   └── Anomalies.png
└── Dashboard.pbix                   # Native Power BI Desktop application file
