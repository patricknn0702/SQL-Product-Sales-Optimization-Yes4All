# SQL-Product-Sales-Optimization-Yes4All
Built a unified dataset from 5+ tables using SQL to analyze 600+ SKUs across Amazon and Walmart. Identified high-ROI categories and created alert logic for sales forecasts, improving promotion targeting and product planning.

# SQL Sales Performance & Forecast Optimization – Yes4All

This project analyzes Yes4All's fitness product sales across Amazon and Walmart, using PostgewSQL to build a unified dataset and drive insights across product contribution, campaign ROI, inventory readiness, and sales trends. The results inform data-driven decisions for marketing spend, portfolio planning, and future launches.

---

## 🎯 Project Goals

- Analyze GMV contribution by product category and subcategory.
- Detect trends and seasonality via month-over-month growth metrics.
- Measure ROI for ad and promotion channels and identify best-performing media levers.
- Evaluate the number and quality of product launches.
- Recommend actions to optimize sales and portfolio balance.
![image](https://github.com/user-attachments/assets/94cb7d57-0be2-4d0b-b069-c03e90ec0219)

![image](https://github.com/user-attachments/assets/461d9223-a18e-4b7d-a436-053db0d61cfa)

![image](https://github.com/user-attachments/assets/39436a95-5c42-46bc-bc9c-676463163d1d)

---

## 🧩 Dataset Overview

- **Source**: Commercial Analyst Case from Yes4All Trading Services, 2024
- **Platforms**: Amazon & Walmart US
- **Tables Used**:
  - `transactions` – sales, ad spend, orders, impressions
  - `product_list` – category/subcategory, launch dates
  - `inventory` – weekly inventory and incoming stock
  - `projection` – forecasted GMV, real sales, marketing costs
  - `event_list` – promotional campaign schedule

---

## 🛠️ Key SQL Operations

- ✅ Created a `master_data` table by joining 5 relational sources
![image](https://github.com/user-attachments/assets/fc5f70b7-04bb-48cd-b8ba-0ed5e48ef209)

- ✅ Performed feature engineering for ad spend, promo spend, total spend, GMV
![image](https://github.com/user-attachments/assets/b37e41cb-d2ef-4fb4-8e63-e4aed73bf08b)

- ✅ Transformed dates and structured sales time series for trend analytics
- ✅ Calculated category- and channel-level ROI
- ✅ Applied logic to check for **forecast reliability** and build alert conditions

---

## 📊 Analysis Highlights

### 1. Sales Contribution by Category

![image](https://github.com/user-attachments/assets/d5390f80-5ca1-4d53-8011-479d6d0cbc02)

![image](https://github.com/user-attachments/assets/ef9cab24-0a41-4716-b499-9953c949b0a4)

- Dumbbells and Exercise Mats accounted for the majority of GMV and ad spend.
- Balance Foam generated the **highest ROI**, outperforming other categories.

### 2. Month-over-Month GMV Trends

![image](https://github.com/user-attachments/assets/e3e503e9-3414-4e6b-8fad-756615a97a61)

![image](https://github.com/user-attachments/assets/c344d630-9096-4a9b-a450-2dbd3ffdf1e1)

- Used `LAG()` and `EXTRACT()` functions to assess monthly growth by category.
- Flagged categories with declining share despite high investment.

### 3. Channel Effectiveness

![image](https://github.com/user-attachments/assets/a6620524-c870-4515-a5ab-3b52da6643af)

- Compared ROI of **Ad Spend** vs. **Promotion Spend**.
- Promotions often showed lower returns (in Balance Foam, Exercise Equipment Mats), prompting reevaluation of cost-efficiency.

### 4. Top vs. Bottom 10 Subcategories
- Top 10 best-selling subcategories
  
![image](https://github.com/user-attachments/assets/5f6bc7c5-fd8c-4c7a-8bab-44efab78d009)

- Bottom 10 selling subcategory

![image](https://github.com/user-attachments/assets/56fac5f9-2fdb-4cd2-beb8-78872d92f381)

- Identified high-potential subcategories for scale-up and low performers for pruning.

### 5. Product Launch Overview
- Tracked number of product launches by month/year.

![image](https://github.com/user-attachments/assets/7ee4faac-a516-4b46-a695-2f83f8be751f)

- 80+ unique SKUs launched in recent cycles; opportunity exists to balance the portfolio.

---

## 🔔 Forecast Logic & Sales Alerts

### SQL-Based Alert Rules:
- ⚠️ *Low Forecasted RS*: If forecasted sales < 3-month average  
- ⚠️ *Inefficient Ad Spend*: If ad spend/GMV ratio drops  
- ⚠️ *Event-Aware*: Adjust alerts during high-sales holiday months

Used these rules to highlight SKUs that may require intervention or deeper analysis.

---

## 💡 Business Recommendations

- **Double down on Balance Foam**: High ROI with relatively low cost base.
- **Reassess investment** in low-ROI categories like heavy dumbbells.
- **Diversify product mix**: Consider testing lighter or seasonal fitness gear.
- **Use alerts** to trigger review of forecast accuracy before inventory lock-in dates.

---

## 📂 Project Files

| File | Description |
|------|-------------|
| `updated_main_code.sql` | Full SQL pipeline and logic |
| `Patrick_finalproject_yes4all_salesdata.pdf` | Final business-facing presentation |
| `Questions-Yes4all Company.docx` | Analyst test prompt and business objectives |

---

## 📌 Key Metrics

| Metric | Value / Insight |
|--------|-----------------|
| SKUs Analyzed | ~600 |
| Categories | Dumbbells, Exercise Mats, Balance Foam, more |
| SQL Views Created | 10+ |
| GMV Contribution Breakdown | By category & channel |
| Alert Logic Rules | 3+

---

## 🧰 Tech Stack

- **PostgreSQL**: Table joins, CTEs, window functions, date handling
- **SQL Analytics**: Trend calculation, ROI modeling, MoM logic
- **Business Logic**: Rule-based alerting, KPI contribution analysis
- *(Optional)* Tableau or Power BI for visual summary

---

## 👤 Author

**Phuoc (Patrick) Nguyen**  
📍 Business Analyst | Growth & Strategy | SQL-Driven Insights  
🎓 MS in Business Analytics, Mercy University, New York  
🔗 [LinkedIn](https://www.linkedin.com/in/phuocnguyenngoc)  
📫 nguyenngocphuoc0702@gmail.com  

