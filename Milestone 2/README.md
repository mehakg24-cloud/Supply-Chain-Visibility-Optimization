# Supply Chain Visibility & Optimization – Milestone 2: Inventory Analytics & Delivery Performance

*This milestone extends the Power BI solution developed in Milestone 1 by introducing two interactive dashboards focused on inventory performance and delivery efficiency. The dashboards leverage DAX measures, KPIs, and interactive visualizations to transform operational supply chain data into actionable business insights.*

---

# Project Overview

This milestone extends the Power BI solution developed in Milestone 1 by adding two interactive dashboards: **Inventory Analytics** and **Delivery Performance**. The dashboards are designed using DAX measures, KPIs, and interactive visualizations to analyze inventory performance and delivery efficiency. The objective is to support better inventory planning, stock management, and logistics decision-making through data-driven insights.

---

# Inventory Turnover Calculation Approach

Inventory turnover measures how efficiently inventory is sold and replenished over a period.

Inventory performance was evaluated using multiple DAX measures to understand stock utilization and inventory efficiency.

### **Key Calculations**

- **Inventory Turnover Ratio (Value)** = **Total Sales ÷ Average Inventory Value**
- **Inventory Turnover Ratio (Units)** = **Units Sold ÷ Average Stock Quantity**

A higher inventory turnover ratio indicates efficient inventory movement and strong product demand, whereas a lower ratio may indicate overstocking or lower product demand.

Additional measures developed include:

- Inventory Turnover Rank
- Total Inventory Value
- Total Stock Quantity
- Warehouse Capacity Utilization
- Month-over-Month Inventory Value Change
- Inventory Value Trend by Region

These measures help evaluate inventory utilization, identify stock movement patterns, and support inventory optimization.

---

# Slow-Moving and Fast-Moving Inventory Identification Logic

Products were classified using the **Stock Status** measure based on:

- **Days Since Last Sale** (number of days since the product was last ordered)
- **Current Stock Quantity**

### **Classification Logic**

| **Condition** | **Stock Status** |
|--------------|------------------|
| Stock Quantity = 0 | Out of Stock |
| Days Since Last Sale > 90 and Stock Quantity > 0 | Dead Stock |
| Days Since Last Sale between 31–90 | Slow-Moving |
| Otherwise | Active |

### **Additional Inventory Measures**

- Dead Stock Count
- Dead Stock Quantity
- Dead Stock Value
- Slow Moving Quantity
- Products to Reorder
- Products Below Safety Stock
- Reorder Quantity Suggested
- Stock Optimization Gap
- Reorder Flag

These measures help identify products that require replenishment, inventory optimization, or clearance strategies, enabling quicker and more informed inventory management decisions.

---

# Delivery Performance Analysis Methodology

Delivery performance was analyzed using DAX measures that compare actual delivery outcomes with planned shipping schedules.

### **Key Calculations**

| **Measure** | **Calculation** |
|-------------|-----------------|
| **On-Time Delivery %** | Orders with **"Shipping on time"** ÷ Total Orders |
| **Late Delivery %** | Orders with **"Late delivery"** ÷ Total Orders |
| **Advance Shipping %** | Orders with **"Advance shipping"** ÷ Total Orders |
| **Lead Time Variance (Days)** | Average Actual Shipping Days − Average Scheduled Shipping Days |
| **Regional Late Delivery Rate** | Late Delivery % calculated for each order region |
| **Late Delivery Trend** | Late Delivery % analyzed over time |
| **Late Delivery Risk %** | Risk Flagged Orders ÷ Total Orders |

Additional measures include:

- Total Orders
- Total Risk Flagged Orders
- Fulfillment Rate
- Risk vs Actual Delivery Accuracy

Interactive visualizations were created to analyze delivery performance across regions, shipping modes, and time using filters and KPIs to provide meaningful operational insights.

---

# Dashboard Features

## Inventory Analytics Dashboard

- Inventory Turnover KPIs
- Dead Stock and Slow-Moving Inventory Analysis
- Inventory Value by Warehouse
- Total Sales by Product Category
- Stock Quantity vs Reorder Level Analysis
- Stock Status Distribution
- Inventory Value Trend by Region
- Interactive filtering for dynamic analysis

## Delivery Performance Dashboard

- On-Time, Late, and Advance Shipping KPIs
- Actual vs Scheduled Shipping Days Comparison
- Regional Late Delivery Analysis
- Late Delivery Risk Analysis
- Delivery Performance Trend Over Time
- Delivery Status Distribution
- Interactive filtering for dynamic analysis

---

# Key Insights

- Inventory turnover metrics help evaluate inventory utilization efficiency across products and warehouses.
- Stock Status classification enables quick identification of Active, Slow-Moving, Dead Stock, and Out of Stock products.
- Warehouse-level inventory analysis highlights locations with higher inventory concentration.
- Reorder level analysis helps identify products approaching replenishment thresholds.
- Delivery performance varies across different regions, helping identify operational improvement opportunities.
- Lead Time Variance and Late Delivery Risk provide valuable insights into shipping efficiency and delivery reliability.
- Trend analysis supports continuous monitoring of inventory movement and delivery performance over time.

---

# Business Recommendations

- Prioritize replenishment for products flagged as **Reorder Now** or **Below Safety Stock**.
- Reduce excess inventory by implementing promotional or clearance strategies for Dead Stock and Slow-Moving products.
- Monitor warehouse capacity regularly to improve inventory distribution.
- Review logistics performance in regions with consistently higher late delivery percentages.
- Improve shipping schedules where Lead Time Variance remains consistently high.
- Continuously monitor inventory turnover and delivery KPIs to support data-driven operational decisions.

---

# Tools Used

- Power BI Desktop
- Power Query
- DAX
- Data Modeling

---

# Project Files

- **Supply_Chain_Milestone_2.pbix**

---

# Dashboards (Screenshots)

### Inventory Analytics Dashboard

`screenshots/Inventory_Analytics_Dashboard.png`

### Delivery Performance Dashboard

`screenshots/Delivery_Analytics_Dashboard.png`

---

# Author

**Mehak Grover**
