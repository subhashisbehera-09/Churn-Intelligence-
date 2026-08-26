
# 📊 Customer Churn Analysis & Intelligence 

**Author:** Subhashis Behera 

**Role:**  Data Analyst

## 📌 Project Overview
Customer churn is one of the most critical metrics for subscription-based businesses. This project focuses on **Customer Churn Analysis and Intelligence** to understand customer behaviors, identify at-risk subscribers, and quantify revenue risk. 

By integrating multi-source datasets (Customer Demographics, Subscriptions, and Support Tickets), this project provides a comprehensive overview of why customers cancel their subscriptions, the escalation correlation with churn, and actionable data-driven insights to improve retention. 

## 🛠️ Tech Stack & Tools Used
* **Python** (Pandas, NumPy, Matplotlib) - Data manipulation, Feature Engineering, and Visualization.
* **SQLite** (sqlite3) - Relational Database Management, SQL queries for dynamic data extraction.
* **Jupyter Notebook** - Interactive data analysis and reporting.
* **Excel** - Initial source data management.

## 🗃️ Data Pipeline & Architecture
1. **Data Ingestion:** Extracted raw data from a multi-sheet Excel file ([customer_churn_data_raw.xlsx](cci:7://file:///c:/Users/Victus/OneDrive/Desktop/panda+sqlite/customer_churn_data_raw.xlsx:0:0-0:0)) and dynamically converted the sheets into relational tables in an **SQLite** database ([customer_churn.db](cci:7://file:///c:/Users/Victus/OneDrive/Desktop/panda+sqlite/customer_churn.db:0:0-0:0)).
2. **Data Extraction:** Dynamically queried the `sqlite_master` to retrieve all tables and load them directly into independent Pandas DataFrames via SQL commands. 
3. **Data Cleaning & Standardization:**
   * Handled missing values via mapping algorithms (e.g., derived missing `Country` data from the `State` column).
   * Rectified and standardized incorrect data types (e.g., date casting).
   * Standardized text inputs (e.g., Gender normalization).
   * Eliminated redundant features and duplicate records.
4. **Data Integration:** Utilized robust SQL-style `LEFT JOINS` within Pandas to merge Customer, Subscription, and Support records into a single holistic analytical dataset.
5. **Data Export:** Serialized the fully cleaned dataset to CSV (`exported_churn_data.csv`) for potential downstream Tableau/PowerBI dashboarding.

## 🚀 Key KPIs & Metrics Analyzed
Through robust feature engineering, several critical business metrics were derived:
* **Churn & Retention Rates:** Baseline tracking of subscriber attrition (28.57% Churn Rate).
* **Churn by Plan Type:** Analyzed attrition across Basic, Standard, and Premium tiers.
* **ARPU (Average Revenue Per User):** Calculated the average revenue generated per active subscription.
* **Average Customer Tenure:** Engineered customer age in days to understand lifetime engagement.
* **Revenue at Risk:** Quantified the exact financial impact (lost revenue) from churned users over a given period.
* **Support Escalation Analysis:** Measured Escalation Rates, Average Complaints per User, and derived a strong **Correlation (0.77) between ticket escalations and churn**.
* **Churn Risk Categorization:** Segmented customers into *Low, Medium, and High* churn risk tiers based on historical behavior scores.

## 📈 Visualizations
Actionable insights were visually represented using **Matplotlib**:
* **Monthly Churn Trend (Time Series):** Highlighted the trajectory of subscriber cancellations over time.
* **Churn Rate by Plan Type (Bar Charts):** Displayed specific churn susceptibilities depending on the user's active plan.

## 💡 Business Value
This project demonstrates an end-to-end data analysis workflow: from raw data extraction and database warehousing to advanced data wrangling and business intelligence reporting. The engineered metrics provide stakeholders with a clear understanding of financial risks and help pivot customer success strategies toward high-risk segments.
