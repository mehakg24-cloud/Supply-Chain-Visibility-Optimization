# Supply Chain Visibility & Optimization – Milestone 4: Warehouse Efficiency & Executive Analytics

This milestone extends the Power BI solution developed in Milestone 3 by adding the **Warehouse Efficiency Dashboard** and the **Executive Dashboard**. The dashboards use DAX measures, KPIs, interactive visualizations, filters, and trend analysis to evaluate warehouse operations and provide a consolidated view of overall supply chain performance.

---

# Project Overview

The **Warehouse Efficiency Dashboard** focuses on warehouse utilization, capacity, stock movement, throughput, and operational performance across different warehouses.

The **Executive Dashboard** provides a consolidated management-level view of important supply chain KPIs from the previous modules, including inventory, delivery, supplier, transportation, and warehouse performance.

The dashboards transform operational supply chain data into meaningful insights that support better capacity planning, inventory management, and supply chain decision-making.

---

# Warehouse Utilization Calculation Methodology

Warehouse utilization was analyzed to measure how effectively available warehouse capacity is being used.

### Key Calculation

**Warehouse Utilization % = Total Stock Quantity ÷ Total Warehouse Capacity × 100**

The utilization percentage helps identify warehouses with higher or lower usage of their available capacity.

The Warehouse Efficiency Dashboard includes:

| **Metric** | **Purpose** |
|------------|-------------|
| **Total Warehouses** | Number of warehouses included in the analysis |
| **Maximum Utilization %** | Highest warehouse utilization level |
| **Minimum Utilization %** | Lowest warehouse utilization level |
| **Average Utilization %** | Overall average warehouse utilization |
| **Warehouse Capacity** | Available capacity of warehouses |
| **Total Stock** | Quantity of inventory stored |
| **Warehouse Units Shipped** | Units shipped through each warehouse |

The dashboard contains **10 warehouses** and provides warehouse-level comparisons using interactive visualizations.

---

# Throughput & Productivity KPI Calculations

Warehouse throughput and productivity were evaluated using stock movement and operational KPIs.

### Key KPIs

| **KPI** | **Calculation / Purpose** |
|---------|----------------------------|
| **Warehouse Units Shipped** | Total quantity of units shipped through each warehouse |
| **Order Count** | Number of orders handled by each warehouse |
| **Total Sales** | Sales associated with each warehouse |
| **Units per Order (Warehouse)** | Warehouse Units Shipped ÷ Order Count |
| **Warehouse Utilization %** | Total Stock Quantity ÷ Warehouse Capacity × 100 |

These measures help compare warehouse activity, throughput, and productivity.

The dashboard also uses a **Total Stock by Warehouse and Average Utilization % by Capacity** analysis to understand the relationship between warehouse capacity, stock levels, and utilization.

---

# Warehouse Performance Analysis

The Warehouse Efficiency Dashboard provides a detailed comparison of warehouse performance.

### Key Analysis Areas

- Warehouse Utilization %
- Warehouse Capacity
- Total Stock Quantity
- Warehouse Units Shipped
- Order Count
- Total Sales
- Units per Order
- Capacity Risk
- Product Category Performance

The dashboard allows warehouse performance to be analyzed using **Warehouse Name, Capacity Risk Flag, and Category Name** filters.

The analysis helps identify warehouses with high utilization, low utilization, higher throughput, and different levels of operational activity.

### Key Warehouse KPIs

| **KPI** | **Dashboard Value** |
|---------|---------------------:|
| **Total Warehouses** | 10 |
| **Maximum Utilization %** | 84.24% |
| **Minimum Utilization %** | 15.93% |
| **Average Utilization %** | 55.15% |

---

# Executive Dashboard Design Methodology

The Executive Dashboard provides a consolidated view of important supply chain performance indicators.

It combines key metrics from the previous dashboards into a single executive-level report.

### Executive KPIs

| **KPI** | **Value** |
|---------|----------:|
| **Total Orders** | 7,104 |
| **Product Categories** | 42 |
| **Fulfillment Rate** | 95.97% |
| **Total Warehouses** | 10 |
| **Total Suppliers** | 118 |
| **Dead Stock Quantity** | 45,605 |
| **Late Delivery %** | 51.22% |
| **Average Supplier Reliability %** | 53.90% |
| **Average Warehouse Utilization %** | 55.04% |
| **Inventory Turnover Ratio** | 0.47x |

The Executive Dashboard also includes:

- Sales trend by order month
- Sales performance by order region
- Late Delivery Risk %
- Average Supplier Reliability %
- Average Warehouse Utilization %
- Inventory Turnover Ratio
- Interactive Market filter
- Interactive Category filter
- Order Date filter
- Executive narrative and summary insights

This design allows management to quickly understand the overall supply chain position and identify areas that require further analysis.

---

# Trend and Forecasting Approach

Time-based trend analysis was implemented using **Order Month** to monitor changes in sales performance over time.

The Executive Dashboard includes a **Total Sales by Order Month** trend visualization covering the available order period.

The trend analysis helps identify changes in sales performance and provides a basis for future planning.

For forecasting, Power BI's time-series forecasting functionality can be applied to suitable date-based measures such as sales trends. Historical order-month data can be used as the basis for estimating future performance and supporting inventory, warehouse, and supply chain planning.

---

# Dashboard Optimization Techniques

The Power BI report was optimized to improve performance, usability, and readability.

### Data and Model Optimization

- Used a structured **Star Schema** data model.
- Used separate Fact and Dimension tables.
- Established relationships between the required tables.
- Removed duplicate records during data preparation.
- Removed unnecessary and redundant columns.
- Added required calculated columns and DAX measures.
- Used appropriate data types and aggregations.

### DAX and Report Optimization

- Created reusable DAX measures for KPI calculations.
- Used appropriate aggregation methods for numerical and categorical fields.
- Used filters and slicers to support focused analysis.
- Organized KPIs and visualizations according to their business purpose.
- Avoided unnecessary visual elements to maintain dashboard readability.

### User Experience Optimization

- Used consistent dashboard layouts and formatting.
- Used KPI cards for important management metrics.
- Used interactive slicers for dynamic analysis.
- Used charts, tables, gauges, and trend visuals to present information clearly.
- Organized detailed warehouse analysis separately from the executive-level summary.

These techniques improve report usability and make the dashboards easier to understand and analyze.

---

# Key Insights

### Executive-Level Insights

- The Executive Dashboard reports **7,104 total orders** with a **95.97% fulfillment rate**, indicating a high overall order fulfillment level.
- The dashboard covers **118 suppliers** and **10 warehouses**, providing a consolidated view of the supply chain network.
- The **Late Delivery % is 51.22%**, highlighting delivery performance as an important area for improvement.
- The **Average Supplier Reliability is 53.90%**, indicating the need for continuous supplier performance monitoring.
- The **Average Warehouse Utilization is 55.04%** in the Executive Dashboard, providing an overall view of warehouse capacity usage.
- The **Inventory Turnover Ratio is 0.47x**, providing an indication of inventory movement efficiency.
- The dashboard reports a **Dead Stock Quantity of 45,605**, highlighting the need for closer monitoring of slow-moving and non-moving inventory.
- Sales trend analysis by order month helps identify changes in sales performance over time.
- Regional sales analysis provides a comparison of sales performance across different order regions.

### Warehouse-Level Insights

- The Warehouse Efficiency Dashboard contains **10 warehouses** for comparison.
- Maximum warehouse utilization reaches **84.24%**, while minimum utilization is **15.93%**, showing significant differences in warehouse capacity usage.
- Average warehouse utilization is **55.15%** in the Warehouse Efficiency Dashboard.
- Warehouse units shipped vary across locations, helping identify differences in warehouse throughput.
- Comparing stock levels with warehouse capacity helps identify differences in storage efficiency.
- Warehouse-level order count, units shipped, total sales, and units per order provide additional measures for comparing productivity.
- Capacity Risk and Category filters allow users to investigate warehouse performance in greater detail.

---

# Business Recommendations

- Monitor highly utilized warehouses regularly to reduce the risk of capacity constraints.
- Improve inventory distribution across warehouses where utilization levels vary significantly.
- Review under-utilized warehouse capacity and identify opportunities for better resource utilization.
- Monitor warehouse throughput, order volume, and units shipped to improve operational planning.
- Use stock quantity and capacity analysis to improve inventory storage efficiency.
- Investigate regions with higher late delivery percentages and improve logistics planning where required.
- Continuously monitor supplier reliability to improve supplier performance and supply continuity.
- Review dead stock levels and consider clearance, promotional, or inventory reduction strategies.
- Monitor inventory turnover to improve stock utilization and reduce unnecessary inventory holding.
- Use the Executive Dashboard for regular management-level monitoring and use detailed dashboards for further operational analysis.
- Use time-based trend analysis and forecasting techniques to support future supply chain and warehouse planning.

---

# Dashboard Features

## Warehouse Efficiency Dashboard

- Total Warehouse KPI
- Maximum Utilization KPI
- Minimum Utilization KPI
- Average Utilization KPI
- Warehouse Units Shipped Analysis
- Average Utilization by Warehouse
- Stock vs Capacity Analysis
- Warehouse Utilization Distribution
- Warehouse Performance Table
- Order Count Analysis
- Total Sales Analysis
- Units per Order Analysis
- Capacity Risk Analysis
- Interactive Warehouse Filter
- Interactive Category Filter

## Executive Dashboard

- Total Orders KPI
- Product Category Count KPI
- Fulfillment Rate KPI
- Total Warehouses KPI
- Total Suppliers KPI
- Dead Stock Quantity KPI
- Late Delivery Risk Gauge
- Average Supplier Reliability Gauge
- Average Warehouse Utilization Gauge
- Inventory Turnover Ratio Gauge
- Total Sales by Order Month Trend
- Sales by Order Region
- Executive Narrative and Summary
- Interactive Market Filter
- Interactive Category Filter
- Interactive Order Date Filter

---

# Tools Used

- **Power BI Desktop**
- **Power Query**
- **DAX**
- **PostgreSQL**
- **Data Modeling**

---

# Project Files

- **Milestone4_PowerBI.pbix**

---

# Dashboards (Screenshots)

## Warehouse Efficiency Dashboard

`screenshots/Warehouse_Efficiency.png`

## Executive Dashboard

`screenshots/Executive_Dashboard.png`

---

# Author

**Mehak Grover**
