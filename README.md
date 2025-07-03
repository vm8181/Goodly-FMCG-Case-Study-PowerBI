## 🧠 Sales Insights Dashboard – FMCG Case Study

This Power BI project was developed as part of the **Goodly Data Case Study Challenge**, focused on building an end-to-end sales performance dashboard for an FMCG distributor. The dashboard is designed to be used by the **National Sales Head (NSH)** and regional teams for tracking KPIs, promotional effectiveness, margin performance, and regional trends.

---

## 📁 Project Overview

- **Domain**: FMCG / Retail Sales
- **Tools**: Power BI, DAX, Power Query, Microsoft Excel
- **Dataset**: Regional sales data, price master, team hierarchy
- **Timeframe**: Multi-year monthly data (2023–2025)
- **Model Structure**: Star schema with Date, Product, Price, Region & Team dimensions

---

## 📊 Dashboard Pages
### 1. 📈 Trend Analysis
- KPI selector: **Sales Value, Gross Profit, Gross Margin (%)**
- Monthly & YoY trends and Seasonal trend based on dynamic last month rolling average
- Dynamic narrative explaining performance patterns
- Forecasting using Compound Annual Growth Rate (CAGR)
- KPI cards, best/worst month flags, and growth indicators

#### Seasonal Trend
![Uploading image.png…]()

#### YoY Trend
![image](https://github.com/user-attachments/assets/43289745-23dc-4d61-9f32-7d814009c4cb)

### 2. 📉 Margin & Promo Analysis
- Promo vs Normal sales segmentation
- Gross margin buckets: High / Mid / Low
- Category-product performance table
- Top products by sales, Promo Share %, and contribution
- Scatter plot for **Promo Share vs Margin %** with recommendations

![image](https://github.com/user-attachments/assets/536740c0-07fe-41a4-925a-88e4cde1d253)

### 3. 🧭 Business Overview
- Regional & team performance (NSM → RSM hierarchy)
- Lost product analysis: SKUs sold last year but not in the selected year
- Lost revenue from dropped SKUs
- Category and region-wise contribution

![image](https://github.com/user-attachments/assets/52a4b9a5-24eb-4be9-beef-32b36429b2ff)

### 3. 🧭 Detailed View (Raw Dataset)

![image](https://github.com/user-attachments/assets/4dc45d92-d368-4e0f-ab51-78ebb1048906)

---

## 🔍 Key Features & Insights

- 📊 **CAGR Forecasting**: `CAGR` to project upcoming FY KPI Values (`Sales`, `Gross Profit`, `Gross Margin%`).
- 💬 **Dynamic Narratives**: Auto-updating text summary based on KPI and time filters
- 🧠 **Q&A Integration**: Supports natural language queries like "top region by sales"
- 🚦 **Promo Effectiveness**: Identifies over-discounting via scatter visual
- 🧩 **Team-Based Filtering**: Enables RSM/NSM level drilldowns
- 📉 **Lost Sales Detection**: Highlights missed opportunities from dropped products


---

## ⚙️ Technical Highlights

- Dynamic File Sourcing with Parameters
  - Implemented a Power Query **parameter** to dynamically source files from a designated folder.
  - Automatically combines regional sales files (**GJ, MH, MP, TG**) using `Folder.Files()` and transforms them into a unified fact table.
  - Supports **folder relocation or deployment reuse** without manually editing queries.
- Custom Calendar Table: Built for the Indian Financial Year (April–March), supporting FY Month-Year, FY Quarter, and correct YTD/QTD logic.
- Parameter-driven KPI selector using `SELECTEDVALUE`
- Time intelligence: `SAMEPERIODLASTYEAR`, `YTD`, `MTD`, `QTD`, `Dynamic Last Month Rolling Average`
- Custom formatting (₹ K / Lac / Cr) using DAX & SWITCH
- Dynamic measure switch logic for narratives and charts
- Use of `EXCEPT`, `RANKX`, and `TOPN` for product loss & regional rank logics

---

## 📌 Evaluation Criteria Met

- ✅ Accurate KPI calculations
- ✅ Dynamic & flexible model
- ✅ Visual clarity & interactivity
- ✅ Business-focused insights & storytelling
- ✅ Scalable with multiple teams & regions

---

## 📂 Folder Structure

- Main Folder
  - ArticlePriceMaster
  - GM Threshold (Created to fulfill the req. `Flexible: Read threshold values from a user-editable input file`)
  - Team
  - Quantity Sales Data stored in folder `Sales Data Table`
    - GJ
    - MH
    - MP
    - TG
