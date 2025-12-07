
# README: Customer Shopping Behavior Analysis Project

## 1. Short Summary

This project conducts an end-to-end analysis of customer shopping behavior using a three-phase pipeline: **Python (Jupyter Notebook)** for data cleaning and preparation, **SQL** for deep analytical querying, and **Power BI** for final reporting and visualization. The goal is to extract key business insights on revenue, product performance, and customer segmentation to drive strategic decision-making.

| Phase | Tool | Purpose | Key Artifact |
| :--- | :--- | :--- | :--- |
| **Preparation** | Python (Jupyter) | Data Cleaning, Feature Engineering, SQL Migration | `Customer_SHopping_Behavior_Python.html` |
| **Analysis** | SQL Queries | Comprehensive metric calculation and segmentation | `CSB_SQL Queries.pdf` |
| **Reporting** | Power BI | Interactive Dashboard and Visualization | `Cust_Shopp_Beha.pbix` |

***

## 2. Detailed Project Overview

### 2.1 Project Goal

To analyze customer shopping data (`customer_shopping_behavior.csv`) and deliver actionable intelligence by quantifying key business metrics, segmenting the customer base, and evaluating marketing/operational factors (e.g., subscriptions, discounts, shipping).

### 2.2 Project Structure and Deliverables

The project consists of three interconnected steps, each corresponding to a major file delivered:

#### Phase 1: Data Ingestion and Preparation (Python)
* **File:** `Customer_SHopping_Behavior_Python.html` (Jupyter Notebook Export)
* **Purpose:** Load the raw CSV, perform data quality checks, handle missing values (e.g., imputing `Review Rating` by category), engineer new features (e.g., creating `age_group` bins), and manage data types.
* **Key Action:** Utilized Python and Pandas functions (`df.info()`, `df.isnull().sum()`, `df.groupby().transform()`, `pd.qcut()`) to clean the data and then execute the **`df.to_sql()`** command to successfully migrate the cleaned dataset to a structured database for SQL querying.

#### Phase 2: Deep Analytical Querying (SQL)
* **File:** `CSB_SQL Queries.pdf`
* **Purpose:** Execute 10 specific, pre-defined SQL queries against the clean database to derive all necessary business metrics and perform segmentation.
* **Key Analytical Areas:**
    * **Revenue:** Calculate revenue by gender (Q1) and age group (Q10).
    * **Marketing:** Compare subscriber vs. non-subscriber performance (Q5), identify high-spend discount users (Q2), and assess discount reliance by product (Q6).
    * **Customer Segmentation:** Define and count customer segments (New, Returning, Loyal) based on purchase history (Q7).
    * **Product:** Find top products by rating (Q3) and top-selling items within each category (Q8), utilizing window functions like **`ROW_NUMBER() OVER (PARTITION BY...)`**.

#### Phase 3: Reporting and Visualization (Power BI)
* **File:** `Cust_Shopp_Beha.pbix`
* **Purpose:** Connect to the SQL-processed data and transform the analytical findings into an interactive, visual dashboard for executive review.
* **Key Components:** The dashboard features visualizations based on the SQL results, including KPI cards, segmented bar charts, pie charts, and interactive filters to enable stakeholders to explore customer trends, product performance, and the impact of promotional strategies.

### 2.3 How to Use the Files

1.  **View Analysis Logic:** Review **`Customer_SHopping_Behavior_Python.html`** for the data cleaning process and **`CSB_SQL Queries.pdf`** for the exact analytical queries used.
2.  **Access Data Insights:** Open **`Cust_Shopp_Beha.pbix`** in Power BI Desktop to interact with the final report, filters, and visualizations of the project's key findings.
3.  **Data Source:** The raw data used for the entire project is **`customer_shopping_behavior.csv`**.



<img width="4872" height="2656" alt="500731798-8bbd5dc9-eb6c-40c1-8f19-c08b4107f654" src="https://github.com/user-attachments/assets/7b43fea3-007a-4bce-8ba6-99c88aa465b0" />
<img width="1275" height="744" alt="Screenshot (163)" src="https://github.com/user-attachments/assets/59827c86-e86d-4c9a-96ed-bbefb271dc8b" />
