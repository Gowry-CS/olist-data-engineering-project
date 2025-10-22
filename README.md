### Data Pipeline Analysing Brazilian E-commerce, Olist Dataset

<img src="Dashboard/Vendor Performance Dashboard.png" alt="Dashboard">

**Goal**

To architect a secure and governed Medallion Lakehouse structure (Bronze, Silver, Gold layers) using Microsoft Fabric and Power BI over a 3-week capstone project with 3 team members. Managed the ELT process for the Olist dataset to create a clean, governed data asset and a high-impact interactive dashboard for stakeholders.

**Project Scope**

1. Creating a centralized, structured dataset from raw Olist E-commerce data from 2016 to 2018. <br> 
2. Automating the data pipeline to support scalable and reproducible analysis. <br>
3. Providing actionable insights and recommendations to the Olist management to make informed decisions on Vendor Performance on the platform.<br>

**Objectives**

- Build an End-to-End Data Engineering Pipeline.

- Implement Vendor Performance Specific Statistics and Generate Insights.

- Visualize Vendor Performance as an Interactive Dashboard for Stakeholders. 


**Data Architecture**

This project was implemented in two main stages: Data Engineering and Data Analysis.

1. Data Engineering Pipeline

- Microsoft Fabric was selected as the optimal data engineering and analytics platform due to its provision of a unified, all-in-one Software-as-a-Service (SaaS) solution.

- Leveraging a Medallion Architecture, the systematic flow of data was ensured, guaranteeing progressive quality, governance, and reliability from raw ingestion to final analytical reporting.

2. Teck Stack
   
- Microsoft Fabric<br> 
- Lakehouses<br> 
- Notebooks (PySpark, PySparkSQL)<br>
- Pipeline Activities: Copy Data, ForEach, Teams Alert<br> 
- Dataflow Gen 2<br> 
- Power BI<br> 

3. Gold Lakehouse Schema

- Galaxy Schema with multiple interconnected Fact tables that share common dimension tables _(refer to documentation page 17)_.

- Created dimension tables (e.g., dim_customers, dim_sellers, dim_dates) and fact tables (e.g., fact_orders, fact_reviews) to allow flexible slicing and dicing of the data.

**Analysis**

- Vendor Metrics and Categorisations for performance benchmarking. 

- Creating a explanatory dashboard to provide stakeholders with a data visualisation for suitable business recommendations _(refer to Power BI Dashboard)_.

- Overall, the At-Risk Vendor category is an immediate priority that needs to be stabilised to mitigate critical customer churn.

- Details on Analysis can be found in the documentation pages 18 - 20.
