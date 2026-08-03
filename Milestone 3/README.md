# Supply Chain Visibility & Optimization – Milestone 3: Supplier Performance & Transportation Analytics

*This milestone extends the Power BI solution developed in Milestone 2 by introducing two interactive dashboards focused on Supplier Performance and Transportation Analytics. The dashboards use DAX measures, KPIs, and interactive visualizations to analyze supplier performance and transportation operations, helping businesses make better decisions.*

---

# Project Overview

This milestone extends the Power BI solution developed in Milestone 2 by adding two interactive dashboards: **Supplier Performance** and **Transportation Analytics**. The dashboards are designed using DAX measures, KPIs, and interactive visualizations to evaluate supplier reliability, supplier quality, transportation efficiency, logistics costs, and shipping performance. The objective is to transform operational supply chain data into meaningful insights that support better supplier management and transportation planning.

---

# Supplier Scorecard Calculation Methodology

Supplier performance was evaluated using multiple DAX measures to analyze supplier quality, reliability, responsiveness, and overall contribution to the supply chain.

### **Key Calculations**

| **Measure** | **Calculation** |
|-------------|-----------------|
| **Total Suppliers** | Distinct Count of Suppliers |
| **Average Quality Score** | Average of Supplier Quality Scores |
| **Average Reliability %** | Average of Supplier Reliability Percentages |
| **Average Lead Time (Days)** | Average Supplier Lead Time |
| **Products Supplied** | Distinct Count of Products Supplied |
| **Orders Fulfilled (Proxy)** | Count of Orders with Status **Complete** or **Closed** |

A **Supplier Composite Score** was calculated using the following weighted formula:

**Supplier Composite Score =**

**(Quality Score × 40%) + (Reliability % × 40%) + (Lead Time Score × 20%)**

where,

**Lead Time Score = ((30 − Lead Time) ÷ 30) × 100**

This weighted approach provides a balanced evaluation by giving higher importance to supplier quality and reliability while also considering supplier responsiveness through lead time.

---

# Supplier Ranking & Benchmarking Approach

Suppliers were ranked using their **Supplier Composite Score**.

The following calculated columns and measures were used:

- Supplier Composite Score
- Supplier Rank
- Reliability Tier
- Low Tier Count
- Medium Tier Count
- High Tier Count

### **Supplier Classification Logic**

| **Condition** | **Reliability Tier** |
|--------------|----------------------|
| Reliability ≥ 80% | High |
| Reliability between 50% and 79% | Medium |
| Reliability < 50% | Low |

Supplier Rank was calculated by ranking suppliers in **descending order** based on their Composite Score. A higher Composite Score indicates better supplier performance.

This approach enables quick identification of high-performing suppliers while highlighting suppliers requiring quality or reliability improvements.

---

# Transportation Cost Analysis Methodology

Transportation performance was evaluated using DAX measures that analyze shipping costs, discounts, profitability, and logistics efficiency.

### **Key Calculations**

| **Measure** | **Calculation** |
|-------------|-----------------|
| **Average Profit Per Order** | Total Profit ÷ Total Orders |
| **Total Discount Given** | Sum of Order Discounts |
| **Average Discount Rate** | Average Discount Percentage |
| **Same Day Share %** | Same Day Orders ÷ Total Orders |
| **Late Rate by Shipping Mode** | Late Delivery % calculated separately for each Shipping Mode |

These measures help evaluate transportation costs, shipping profitability, discount strategies, and delivery performance across different shipping modes.

---

# Route & Carrier Performance Evaluation

Transportation performance was further analyzed using interactive visualizations to compare different shipping modes, delivery efficiency, and regional transportation performance.

The dashboard includes:

- Total Discount by Shipping Mode
- Average Profit Per Order by Shipping Mode
- Late Rate by Shipping Mode
- Shipping Mode Distribution
- Late Delivery Heat Map (Market vs. Order Region)
- Date-wise Transportation Analysis
- Interactive slicers for Market and Order Date

These visualizations help identify shipping modes with higher transportation costs, evaluate delivery performance across different markets, and monitor transportation trends over time.

---

# Dashboard Features

## Supplier Performance Dashboard

- Supplier Performance KPIs
- Supplier Scorecard
- Supplier Composite Score Analysis
- Supplier Tier Distribution
- Supplier Quality Score Distribution
- Lead Time vs. Reliability Scatter Analysis
- Supplier Benchmarking Table
- Interactive filtering by Supplier and Product

## Transportation Analytics Dashboard

- Transportation Cost KPIs
- Shipping Mode Performance Analysis
- Discount Analysis
- Profitability Analysis
- Late Delivery Analysis by Shipping Mode
- Transportation Heat Map
- Interactive filtering by Market and Order Date

---

# Key Insights

- Supplier Composite Score provides an overall evaluation by combining supplier quality, reliability, and lead time.
- Reliability Tier classification enables quick identification of High, Medium, and Low-performing suppliers.
- Quality Score distribution helps benchmark supplier performance across the supplier network.
- Scatter analysis highlights the relationship between supplier lead time and reliability.
- Transportation cost analysis helps monitor discounts, profitability, and logistics expenses.
- Shipping mode comparison identifies differences in transportation efficiency and late delivery performance.
- Heat map analysis highlights regional variations in transportation performance across different markets.

---

# Business Recommendations

- Prioritize procurement from suppliers with higher Composite Scores and Reliability Tiers.
- Collaborate with lower-performing suppliers to improve reliability and product quality.
- Reduce supplier lead times wherever possible to improve overall supply chain responsiveness.
- Continuously monitor supplier performance using scorecards and benchmarking metrics.
- Review shipping modes with higher late delivery rates and transportation costs.
- Optimize transportation planning by analyzing regional performance and logistics trends.
- Monitor discount strategies regularly to maintain profitability while supporting customer demand.

---

# Tools Used

- Power BI Desktop
- Power Query
- DAX
- Data Modeling

---

# Project Files

- **Milestone3_PowerBI.pbix**

---

# Dashboards (Screenshots)

### Supplier Performance Dashboard

`screenshots/Supplier_Scorecard_Dashboard.png`

### Transportation Analytics Dashboard

`screenshots/Transportation_Analytics_Dashboard.png`

---

# Author

**Mehak Grover**
