### Data Pipeline Analysing Brazilian E-commerce, Olist Dataset

**Goal**

To architect a secure and governed Medallion Lakehouse structure (Bronze, Silver, Gold layers) using Microsoft Fabric and Power BI over a 3-week capstone project with 3 team members. Managed the ELT process for the Olist dataset to create a clean, governed data asset and a high-impact interactive dashboard for stakeholders.

Through this project, we aim to:

1. Extract Data from different sources though an ETL/ELT pipeline to a database.<br>
2. Develop a well-structured database schema to support scalable and reliable analysis.<br>
3. Assess whether rainfall influences emergency room admissions.<br>
4. Evaluate the reliability of weather forecasts for planning hospital resources.<br>

**Scope & Limitations**

**Scope**

- Focuses on emergency cases, historical rainfall data, and historical rainfall forecast data from 2003 to 2004.

- Includes data from most public hospitals in Singapore during this period. Data source links are provided in the [Documentation](https://github.com/Gowry-CS/emergency-cases-weather-pipeline/blob/main/Emergency%20Cases%20and%20Weather%20Correlation%20Documentation.pdf)
 (PDF, page 2).

- Designed and implemented a database schema optimized for OLAP queries, enabling efficient trend and correlation analysis.

- Refer to the [Final Database Schema ERD diagram](https://github.com/Gowry-CS/emergency-cases-weather-pipeline/blob/main/Final%20Database%20Design/Final%20Database%20Design.png) for an overview of the relationships between tables. 

Concentrates on two core research questions:<br>

1.Does rainfall influence emergency room admissions?<br>
2.Are weather forecasts sufficiently reliable for planning hospital resources?

*All Jupyter notebooks and SQL scripts have been numbered accordingly for anyone to be able to recreate the data flow from the data sources to the staging database and final database in PostgreSQL*  

**Limitations**

- Woodlands Health was excluded as it was not operational during the study period.<br>
- KKH was excluded due to unavailable data via MOH.<br>
- Analysis is restricted to the 2003–2004 timeframe; insights may not generalize to current hospital operations or climate patterns.<br>
- Weather and healthcare data availability may introduce bias or gaps in certain time intervals. <br>

**Methodology**

This project was implemented in two main stages: Data Engineering and Data Analysis.

1. Data Engineering (ETL Pipeline)

- Extract: Collected weather and healthcare datasets from publicly available sources.

- Transform: Cleaned, standardized, and joined datasets to ensure consistency (e.g., date formats, missing values, and categorical encoding).

- Load: Stored the processed data into a structured database optimized for analytical queries.

2. Database Design

- Designed a star schema to support OLAP queries, improving efficiency for aggregation and correlation analysis in the Gold Lakehouse.

- Created dimension tables (e.g., dim_customers, dim_sellers, dim_dates) and fact tables (e.g., fact_orders, fact_reviews) to allow flexible slicing and dicing of the data.

3. Analysis

- Conducted exploratory queries to examine .

- Creating a explanatory dashboard to provide stakeholders with a data visualisation for suitable business recommendations.

- Details on Analysis can be found in the [presentation](https://github.com/Gowry-CS/emergency-cases-weather-pipeline/blob/main/Emergency%20Cases%20and%20Weather%20Correlation%20Presentation.pdf) slides 19-24.
