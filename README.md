# Krazy Kitchen Data Warehouse

Krazy Kitchen is a restaurant known for its innovative cuisine and diverse menu. This project addresses the challenges of managing reservations, inventory, customer orders, and employee data by implementing a comprehensive data warehouse. The solution enables centralized data management, seamless integration, and advanced analytics to enhance decision-making and operational efficiency.

## Table of Contents
- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Data Warehouse Design](#data-warehouse-design)
- [ETL Pipeline](#etl-pipeline)
- [Cloud Implementation](#cloud-implementation)
- [Data Visualization](#data-visualization)
- [Technologies Used](#technologies-used)
- [Contributors](#contributors)

## Introduction
Krazy Kitchen faces difficulties in analyzing data for informed decision-making. This project delivers a cloud-based data warehouse to consolidate data from various sources, streamline operations, and provide actionable insights.

## Problem Statement
The restaurant requires a scalable and efficient data warehouse to:
- Integrate data from multiple sources.
- Perform detailed analytics on sales, inventory, and employee performance.
- Support data-driven decision-making to boost profitability.

## Objectives
- **Centralized Data Repository:** Consolidate operational data (reservations, inventory, orders, staff schedules).
- **Advanced Analytics:** Generate insights into sales trends and customer behavior.
- **Seamless Integration:** Merge data from existing systems and external sources.
- **ETL Automation:** Facilitate smooth extraction, transformation, and loading processes.
- **Improved Decision-Making:** Support growth with data-driven strategies.

## Data Warehouse Design
The data warehouse employs a star schema with the following elements:
- **Fact Table:** Sales data, including metrics like total sales, quantity, and discounts.
- **Dimension Tables:** Customers, dishes, staff, time, orders, and receipts.
- **Hierarchies:** Time and staff hierarchies for flexible queries.

## ETL Pipeline
The ETL pipeline was implemented using Talend Studio and AWS Glue:
- **Source Files:** Data extracted from CSV and JSON files.
- **Transformation:** Schema adjustments, surrogate key generation, and derived measures (e.g., discount amount).
- **Loading:** Data stored in S3 as Parquet files, enabling efficient querying via AWS Athena.

## Cloud Implementation
The data warehouse is hosted on AWS for scalability and reliability:
- **AWS S3:** Stores raw and transformed data.
- **AWS Glue:** Automates schema inference, ETL code generation, and job execution.
- **AWS Athena:** Performs SQL-based queries on the data warehouse.
- **AWS Lambda:** Handles event-driven tasks.

## Data Visualization
Dashboards were created using Power BI and Tableau to:
- Analyze sales trends and dish performance.
- Support drill-down and roll-up operations for detailed insights.

## Technologies Used
- **Database:** PostgreSQL
- **ETL Tools:** Talend Studio, AWS Glue
- **Storage:** AWS S3, Parquet files
- **Querying:** AWS Athena
- **Visualization:** Power BI, Tableau
- **Programming:** Python

## Contributors
- [Rohan Reddy Pathi](pathi.r@northeastern.edu)
- [Laawanyaa Sai thota](thota.l@northeastern.edu)
