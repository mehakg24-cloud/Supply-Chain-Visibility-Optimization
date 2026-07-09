<h1 align="center">Supply Chain Visibility & Optimization – Milestone 1: Data Modelling</h1>

<p align="center">
Building a scalable and optimized Star Schema data model for Supply Chain Analytics using Power BI, Power Query and DAX.
</p>

---

# Project Overview

This repository contains **Milestone 1** of the **Supply Chain Visibility & Optimization** project developed using **Power BI**. The primary focus of this milestone is to transform a raw supply chain dataset into a well-structured **Star Schema** data model through data preprocessing, dimensional modeling, relationship management, and DAX calculations. The resulting model provides a strong foundation for future dashboards and business analytics.

---

# Objective

The objective of this project is to:

- Import the Supply Chain dataset into Power BI.
- Perform data cleaning and preprocessing using Power Query.
- Handle duplicate records and apply necessary data transformations.
- Create Fact and Dimension tables following the Star Schema approach.
- Define relationships between the tables to support business analysis.
- Create reusable DAX calculations.
- Prepare the data model for future dashboard development.

---

# Dataset Source

| Item | Details |
|------|---------|
| **Dataset** | DataCo Smart Supply Chain Dataset |
| **Source** | Kaggle |
| **Link** | https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis |
| **Records** | Approximately 180,519 |
| **Columns** | 53 |

The dataset contains information related to customers, products, categories, departments, shipping, locations, sales, orders and profits.

---

# Tools Used

| Tool | Purpose |
|------|---------|
| Power BI Desktop | Data Modeling |
| Power Query | Data Cleaning & Transformation |
| DAX | Calculated Tables & Measures |
| GitHub | Project Repository & Version Control |

---

# Data Cleaning and Transformation Steps

The following transformations were performed using **Power Query**:

- Imported the Supply Chain dataset into Power BI.
- Renamed the primary table as **Fact_table**.
- Removed unnecessary columns including:
  - Customer Email
  - Customer Password
  - Order Zipcode
- Created separate Dimension Tables by duplicating the Fact Table.
- Selected only the required columns for each Dimension Table.
- Removed duplicate records using the appropriate key columns.
- Created **Location_id** using an Index column in the Location table.
- Merged the Location table with the Fact Table.
- Created **Dim_Date** using DAX.
- Added Year, Month Number, Month, Quarter, Week, Day and Day Name columns to the Date table.
- Applied all transformations using **Close & Apply**.

---

# Data Model Overview

The project follows the **Star Schema** architecture by organizing the dataset into one central Fact Table and multiple Dimension Tables.

## Fact Table

| Table | Description |
|--------|-------------|
| **Fact_table** | Stores transactional supply chain records including customer, product, order, shipping and sales information. |

## Dimension Tables

| Table | Description |
|--------|-------------|
| **Dim_Customer** | Customer information |
| **Dim_Product** | Product information |
| **Dim_Category** | Product category information |
| **Dim_Department** | Department details |
| **Dim_Shipping** | Shipping and delivery information |
| **Dim_Location** | Geographic location information |
| **Dim_Date** | Calendar and time-related information |

Relationships were created between the Fact Table and Dimension Tables to support efficient filtering, reporting and business analysis.

The completed data model is available in the **screenshots** folder.

---

# DAX

A **Dim_Date** table was created using **DAX**.

The following date attributes were added:

- Year
- Month Number
- Month
- Quarter
- Week
- Day
- Day Name

Reusable business measures such as **Total Sales**, **Total Orders**, **Total Profit**, **Average Order Value**, **Sales Growth**, and customer-related calculations are documented in **DAX_Measures.txt**.

---
---

# Skills Demonstrated

- Data Cleaning
- Data Transformation
- Power Query
- Data Modeling
- Star Schema Design
- Relationship Management
- DAX
- Business Intelligence

---

# Future Scope

This data model can be extended further by developing interactive Power BI dashboards for:

- Sales Analysis
- Customer Analysis
- Shipping Performance
- Product Performance

---

# Author

Mehak Grover
