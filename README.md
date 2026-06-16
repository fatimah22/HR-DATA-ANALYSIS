# HR Analytics Dashboard (2M Employees)

## Overview
This project presents an end-to-end **HR Analytics Dashboard** built using **SQL Server** and **Power BI** on top of a large HR dataset of approximately **2 million employee records**.

The goal of the project is mainly **technical**: handling high-volume data, cleaning and preparing it in SQL, then delivering a clean, performant data model and interactive HR dashboard in Power BI.

## Project Goal
- Clean and prepare a large HR dataset (2M rows) using SQL Server.
- Build an efficient, analysis-ready view as a single entry point for Power BI.
- Design HR KPIs and visuals that can scale with large data.
- Demonstrate an end-to-end workflow from raw data to interactive dashboard.

## Tools Used
- **SQL Server** — data cleaning, transformation, derived columns, and views.
- **Power BI** — data modeling, DAX measures, and dashboard design.
- **Power Query** — additional shaping inside Power BI where needed.

## Dataset
- Sample HR dataset (~2,000,000 employee records).
- Fields include: employee status, department, job role, salary bands, performance, work mode, hire dates, experience, and attrition flags.
- Data is **synthetic/sample**, designed to be balanced across departments, so the focus is on the **technical pipeline** more than discovering dramatic business patterns.

## 1. Data Preparation in SQL Server
Because of the dataset size, it was not efficient to load everything raw into Power BI.  
Instead, the data was pre-processed in SQL Server, and only a clean, aggregated layer was exposed to Power BI.

Main SQL tasks included:
- Testing data quality and cleaning text values.
- Filtering only required columns for reporting.
- Creating **derived columns** such as:
  - `Tenure_Years` to calculate length of service.
  - Numeric flags for employee status to support attrition calculations.
- Creating a **SQL View** so that Power BI reads from a single, organized source.

Key idea:
- Heavy calculations (like tenure and status flags) are done in SQL once, instead of repeating them on every row in Power BI.
- This helps keep the model performant even when slicing by year, department, job role, and other dimensions.

## 2. Data Modeling and Measures in Power BI
After preparing the view in SQL Server, it was connected as the main data source in Power BI.

Core steps:
- Import the cleaned view into Power BI.
- Build relationships and organize the data model.
- Create DAX measures for key HR metrics, such as:
  - `Total Employees`
  - `Active Employees`
  - `Attrition Employees`
  - `Attrition Rate`
  - `Average Salary`
  - Other HR-related KPIs

With a large dataset, it was important that measures rely on **ready, well-structured columns** coming from SQL to maintain good performance in Power BI.

## 3. Dashboard Pages
The report is organized into several pages, each focusing on a specific HR perspective:

1. **Workforce Overview**
   - Headcount and active vs. attrition employees.
   - Distribution by department.
   - Work mode distribution (e.g. on-site, hybrid, remote).

2. **Attrition**
   - Attrition rate over time.
   - Attrition by department.
   - Attrition by salary band.
   - Attrition by performance and tenure.

3. **Compensation**
   - Salary evolution over years.
   - Average salary by department and job role.
   - Compensation distribution views.

4. **Performance**
   - Performance rating distribution.
   - Average performance by department.
   - Comparison of performance across segments.

Because the dataset is balanced and synthetic, many metrics appear similar across departments.  
For this reason, the primary focus of the project is **technical implementation and scalability**, not deep real-case HR storytelling.

## Key Skills Demonstrated
- Handling large datasets (~2M rows).
- Data cleaning and transformation in **SQL Server**.
- Creating **SQL views** as a clean layer for BI tools.
- Building a structured data model in **Power BI**.
- Writing DAX measures for HR KPIs.
- Designing HR dashboards with clear pages and navigation.
- Balancing performance and flexibility for slicing and filtering.

## Notes
- The data used in this project is **sample data**, not real company data.
- The main objective is to demonstrate the **end-to-end pipeline** from SQL to Power BI for HR analytics at scale.

---

## About the Analyst
Hi, I'm **Fatimah Bin Awdhah**, a Data Analyst with engineering background. 
I specialize in Power BI dashboards, data cleaning, and turning business data into clear, actionable insights.

- 🌐 Portfolio: [fatimah-data-portfolio.netlify.app](https://fatimah-data-portfolio.netlify.app/)
- 💼 LinkedIn: [linkedin.com/in/fatimah-alodah](https://www.linkedin.com/in/fatimah-alodah)
- 📧 Contact: feel free to connect with me on LinkedIn



