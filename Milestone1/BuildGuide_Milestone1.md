# Milestone 1 – Build Guide (Power BI)

## Project Overview

This project uses the DataCo Smart Supply Chain Dataset to build a dimensional data model in Power BI. The raw dataset was cleaned, transformed, and converted into a Star Schema to improve reporting and analytical performance.

---

## Step 1 – Import Dataset

- Open Power BI Desktop.
- Select **Get Data → Text/CSV**.
- Choose the DataCo Supply Chain CSV file.
- Click **Transform Data** to open Power Query Editor instead of loading the data directly.

---

## Step 2 – Data Preparation

The dataset was cleaned and transformed in Power Query before loading into the model.

The following operations were performed:

- Removed unnecessary columns such as Customer Email, Customer Password and Order Zipcode.
- Removed duplicate records wherever required.
- Verified appropriate data types for date, numeric and text fields.
- Renamed the base query as **Fact_table**.

---

## Step 3 – Create Dimension Tables

The Fact_table was duplicated to create separate dimension tables.

The following tables were created:

- Dim_Customer
- Dim_Product
- Dim_Category
- Dim_Shipping
- Dim_Location
- Dim_Department
- Dim_Date

Each dimension contains only the required attributes and duplicate values were removed to maintain unique records.

---

## Step 4 – Build Relationships

Relationships were created between the fact table and dimension tables to form the data model.

The model includes:

- Customer → Fact Table
- Product → Fact Table
- Category → Product
- Shipping → Fact Table
- Location → Fact Table
- Department → Fact Table
- Date → Fact Table

The model follows a Star Schema structure suitable for business intelligence reporting.

---

## Step 5 – Date Table

A separate Date dimension was created using DAX.

Additional columns generated include:

- Year
- Month
- Month Number
- Quarter
- Week
- Day
- Day Name

This enables time-based analysis and reporting.

---

## Step 6 – Save & Documentation

After validating relationships, the Power BI project was saved as a PBIX file.

The GitHub repository includes:

- Power BI project file
- Star schema reference tables
- Data model screenshot
