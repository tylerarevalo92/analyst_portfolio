# Healthcare Analytics Portfolio

A portfolio of business analyst projects in **PostgreSQL**, **Tableau**, and **Excel**.  
This repository showcases my ability to work with real-world healthcare datasets, perform data cleaning and transformation, and create insights through visualizations and dashboards.  

---

## 🔹 Project Overview
Healthcare analytics plays a critical role in improving patient outcomes, reducing costs, and driving data-driven decision making.  
This portfolio highlights end-to-end data work, including:

- **Database Setup & Management**: Running PostgreSQL in Docker for a clean, reproducible environment.  
- **Data Exploration**: Using DBeaver for SQL development, schema design, and dataset exploration.  
- **Data Analysis**: Cleaning and transforming CMS public healthcare datasets (e.g., Hospital Readmissions Reduction Program).  
- **Visualization & Reporting**: Building dashboards in Tableau Public and creating reports in Excel.  

---

## 🔹 Completed Work
- Set up **PostgreSQL** inside Docker for a local development environment.  
- Connected the database to **DBeaver** and imported CMS HRRP dataset:  
  - Columns: Facility Name, Facility ID, State, Measure Name, Discharges, Readmission Ratios, Rates, etc.  
  - Cleaned data (handling `N/A` values, parsing dates, converting numeric fields).  
- Verified and prepared dataset for analysis in SQL.
  
- Created the HRRP Readmissions Table
  - Raw Table (hrrp_readmissions_raw)
  - All columns imported as TEXT. Preserves raw data including placeholders like N/A and Too Few to Report.
- Created Cleaned Table (hrrp_readmissions)
  - Replaces N/A and Too Few to Report with NULL.
  - Converts numeric fields (number_of_discharges, excess_readmission_ratio, predicted_readmission_rate, expected_readmission_rate) to INT or NUMERIC.
  - Converts date strings (start_date and end_date) to DATE.
- Key SQL Techniques Used
  - NULLIF(column, 'N/A') – replaces placeholders with NULL.
  - CAST(... AS INT/NUMERIC) – converts text to numeric types.
  - CASE statement – handles special conditions like "Too Few to Report".
  - TO_DATE(..., 'MM/DD/YYYY') – converts text to date type.
- Created Hospital General Info Table
  - Raw Table (hospital_general_info_raw)
  - Imported all columns as TEXT. Preserves raw values, including "Not Available".
- Created Cleaned Table (hospital_general_info_clean)
  - Replaces "Not Available" with NULL.
  - Converts numeric fields (measure counts, scores) to INT.
  - Keeps textual footnotes and descriptors intact.
- Key SQL Techniques Used
  - NULLIF(column, 'Not Available') – converts placeholder text to NULL.
  - CAST(... AS INT) – converts numeric columns to integers.
  - Organized in sections (MORT, Safety, Readmissions, Patient Experience, Timely & Effective Care) for clarity.
- Benefits of This Approach
  - Data Integrity: Cleaned numeric and date fields are ready for analysis.
  - Reproducibility: DROP TABLE IF EXISTS ensures scripts can be run multiple times safely.
  - Scalability: Can be extended to additional hospital measures or datasets.
  - Transparency: Clear comments and sectioning make the process understandable to others.
---

## 🔹 In Progress
- Designing **SQL queries** to explore key healthcare questions:  
  - Which Arizona hospitals have the highest/lowest excess readmission ratios?  
  - How do predicted vs expected readmission rates compare across measures?  
  - Are there trends by condition (AMI, HF, PN, etc.) over time?  

---

## 🔹 Planned Work
- **Tableau Dashboards (Public Profile)**  
  - Dashboard 1: Readmission rates in Arizona vs national averages  
  - Dashboard 2: Hospital-level comparisons by condition  
  - Dashboard 3: Trend analysis of predicted readmission rates (2020–2023)  

- **Excel Reports**  
  - Summary tables and pivot charts for healthcare quality metrics  
  - Supplementary visuals to highlight insights  

- **Additional Datasets (Future Expansion)**  
  - Medicare Spending per Beneficiary  
  - Hospital Compare (quality ratings, mortality, safety)  
  - Healthcare Costs by Condition  

---

## 🔹 Tools & Technologies
- **Database**: PostgreSQL (Dockerized)  
- **SQL IDE**: DBeaver  
- **Visualization**: Tableau Public, Excel  
- **Languages**: SQL (Postgres), Excel formulas/pivots  

---

## 🔹 Live Dashboards & Reports
👉 [Readmission Rates in Arizona vs National Average](#)  
👉 [Hospital-Level Comparisons by Condition](#)  
👉 [Readmission Rate Trends (2020–2023)](#)  

*(links will be updated as Tableau Public dashboards are published)*  

---

## 🔹 Portfolio Goals
This portfolio demonstrates:
- SQL proficiency in cleaning, transforming, and analyzing healthcare data.  
- Ability to design and publish professional dashboards in Tableau.  
- Analytical skills applied to real-world healthcare quality metrics.  
- A reproducible workflow using open datasets and open-source tools.  

---

📌 Stay tuned — as I add new dashboards and datasets, I’ll update this repository with screenshots, SQL scripts, and links to interactive Tableau projects.  

