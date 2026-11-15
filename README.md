# Superstore Sales & Profitability Dashboard (2014–2017)

**Elevate Labs – Data Analyst Internship (Task 4: Dashboard Design)**  
An interactive Power BI dashboard built to help business stakeholders monitor retail revenue, profit margins, multi-year growth trends, and regional/product performance.

---

## 📊 Dashboard Preview

![Superstore Dashboard Preview](screenshots/dashboard_preview.png)

---

## 🎯 Project Objectives
- Track top-line business health using dynamic **KPI summary cards** (Sales, Profit, Profit Margin, Total Orders).
- Analyze multi-year revenue and profit trajectories using **time-series area charts**.
- Identify top-performing states and flag unprofitable sub-categories to guide pricing and discount decisions.
- Enable self-service exploration through interactive **slicers** and cross-visual filtering.

---

## 🛠️ Tools & Techniques Used
- **BI Tool:** Microsoft Power BI Desktop
- **Data Cleaning:** Power Query (type enforcement for dates, currency decimals, and text postal codes)
- **Data Modeling & DAX:** Dedicated `_Measures` table for calculated KPIs
- **Dataset:** [Superstore Dataset (Kaggle)](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

---

## 📐 Core DAX Measures

```dax
Total Sales = SUM('Sample - Superstore'[Sales])

Total Profit = SUM('Sample - Superstore'[Profit])

Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)

Total Orders = DISTINCTCOUNT('Sample - Superstore'[Order ID])

Total Quantity = SUM('Sample - Superstore'[Quantity])