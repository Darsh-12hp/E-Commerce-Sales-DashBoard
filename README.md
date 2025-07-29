
# E-commerce Sales Dashboard - Power BI

##  Project Overview
This Power BI dashboard provides a detailed performance overview of an e-commerce business. 
It includes real-time visual insights on sales, profit, shipping performance, regional breakdown, product performance, and trends across time periods.

---

## 🧾 Data Source
 
  - CSV
  - PG SQL Server 


## Key Metrics & DAX Measures

###  Main KPIs Displayed
- **YTD Sales**
- **YTD Profit**
- **YTD Quantity**
- **YTD Profit Margin**
- **YoY Sales Growth**
- **Top/Bottom Products by YTD Sales**
- **Sales by Region, State, and Shipping Type**

###  Sample DAX Measures

```DAX
-- Profit Margin
Profit Margin = DIVIDE(SUM(Profit), SUM(Sales))

-- YoY Sales %
YOY Sales = DIVIDE([YTD Sales] - [PYTD Sales], [PYTD Sales])

-- Trend Icon
Profit Margin ICON = 
VAR positive_icon = UNICHAR(9650)  // ▲
VAR negative_icon = UNICHAR(9660)  // ▼
RETURN IF([YOY Profit Margin] >= 0, positive_icon, negative_icon)
