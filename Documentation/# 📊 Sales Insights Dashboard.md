# 📊 Sales Insights Dashboard – Power BI Case Study

This Power BI project was developed as part of a case study to deliver a scalable and insightful sales performance dashboard for an FMCG distributor. It is intended for use by the **National Sales Head (NSH)** and their team to track regional sales, profitability, promotions, and team performance across hierarchies.

---

## 📦 Dataset Overview

### 1. 📈 Quantity Sales Data (Excel Files)
- One file per region: `GJ`, `MH`, `MP`, `TG` — stored in folder **"Sales Data Table"**
- Each file contains multiple sheets (e.g., 2023, 2024)
- Each sheet contains **monthly product-wise quantity sold**

### 2. 💰 Selling Price Master (CSV)
- Fields include:
  - Product-wise, month-wise **Selling Price**
  - **Cost Price**
  - **Base Price**
- Sales Type is derived based on base price:
  - If **Selling Price < Base Price** → `Promo`
  - Else → `Normal`
- Logic implemented via Power Query or DAX
- Enables sales analysis by:
  - **Sales Type** (Promo / Normal)
  - **Time Period**
  - **Region** and **NSM**

### 3. 👥 Sales Team Structure (Excel File)
- Defines hierarchy:
  - **Sales Rep → Area Manager → Regional Head → NSM**
- Used to enable **team-level reporting** and **filtering**

---

## 📝 Deliverables

Prepare a Power BI report with the following three report pages:

---

### 1️⃣ Trend Analysis Page
Design a KPI-driven trend view including:
- Monthly trends for:
  - **Sales Value**
  - **Gross Profit**
  - **Gross Margin (%)**
  - With **Year-over-Year (YoY)** comparison
- KPI Selector:
  - Single chart that updates dynamically based on selected KPI
  - Dynamic chart title and number formatting
- Align all date logic with **Indian Financial Year (April–March)**

---

### 2️⃣ Margin & Promo Analysis Page

#### 2.1 Category-Product Sales Table
- For each **product category**, show:
  - Total Sales
  - **Sales Mix %**
  - **Promo Sales Share %**
  - Top 3 Products (by Sales Value)

#### 2.2 Margin Segmentation Visual
- Bucket products based on **Gross Margin %**:
  - **High Margin**: > 50%
  - **Mid Margin**: 30–50%
  - **Low Margin**: < 30%
- Segmentation logic should be:
  - **Flexible** – values read from user-editable file
  - **Dynamic** – adjusts with selected Year & Quarter
- For each bucket, display:
  - Total Sales
  - Revenue Growth % (vs. previous period)
  - Gross Margin %
- Visual should:
  - Cross-filter the **Category-Product Table**
  - Be a matrix, donut, or stacked column chart

#### 2.3 Slicers
- Year
- Quarter (as Q1, Q2, Q3, Q4)

---

### 3️⃣ Business Overview Page
- Provides a high-level view of:
  - Total sales, margin trends
  - Top-performing regions and categories
- Critical insight:
  - **Count of products sold in the previous year but not sold in the selected year**
  - **Total lost sales value from dropped SKUs**

---

## ✅ Evaluation Criteria

Your solution will be assessed based on:

- ✅ **Accuracy** of calculations:
  - Sales Type, Gross Margin, YoY logic
- ✅ **Scalability** and efficiency of the data model
- ✅ **Flexibility**:
  - Measures react to filters and parameters
- ✅ **Clarity** of visuals and overall report design

---

## ⚙️ Technical Requirements

- The model should be **dynamic** and allow **folder path parameterization** for dataset input.
- Ensure the **file structure remains unchanged** for deployment and reuse.

---

## 📎 Dataset Provided

`Task1 Sales Dashboard.zip` (includes sales data, price master, team structure)

---

## 🔗 Submission

Please provide:
- A link to download your `.pbix` file  
**or**
- Upload the Power BI file directly as part of your application submission.

---

Let me know if you'd like me to generate a downloadable `README.md` file or a GitHub-friendly version with embedded visuals or repo structure! 
