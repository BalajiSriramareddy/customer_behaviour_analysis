# Customer Behaviour Analysis (Data Analytics Project)

## Overview
This project analyses customer shopping behaviour to uncover patterns in **spend, product preferences, seasonality, discounts/promos, shipping choices, and repeat purchasing**. It follows an end-to-end analytics workflow: **Python (EDA + cleaning) → SQL (insights + BI-ready views) → Power BI (dashboard) → Report → Presentation (Gamma).**

Dataset used: Kaggle “Customer Shopping Behaviour Analysis” by Warda Bilal. :contentReference[oaicite:0]{index=0}

---

## Dataset
**Source:** Kaggle (Customer Shopping Behaviour Analysis) :contentReference[oaicite:1]{index=1}  
**Rows / Columns:** **3,900 rows × 19 columns** :contentReference[oaicite:2]{index=2}  
**Typical file name:** `shopping_trends.csv` (commonly used in analyses of this dataset) :contentReference[oaicite:3]{index=3}  

**Columns**
- Customer ID
- Age
- Gender
- Item Purchased
- Category
- Purchase Amount (USD)
- Location
- Size
- Color
- Season
- Review Rating
- Subscription Status
- Payment Method
- Shipping Type
- Discount Applied
- Promo Code Used
- Previous Purchases
- Preferred Payment Method
- Frequency of Purchases :contentReference[oaicite:4]{index=4}

---

## Tools & Tech Stack
**Python**
- pandas, numpy
- matplotlib / seaborn
- Jupyter Notebook

**SQL**
- PostgreSQL / MySQL / SQL Server (schema + queries + views)

**BI**
- Power BI (data model, DAX measures, interactive visuals)

**Deliverables**
- Report (PDF/DOCX)
- Presentation (Gamma)

---

## Project Steps
1. **Load dataset (Python)**
   - Import CSV
   - Validate schema, datatypes, missing values, duplicates

2. **EDA (Python)**
   - Spend distribution and outliers (Purchase Amount)
   - Category / item popularity
   - Seasonality trends
   - Discount & promo impact on spend
   - Subscription vs non-subscription behaviour
   - Repeat purchasing signals (Previous Purchases, Frequency of Purchases)

3. **Data Cleaning (Python)**
   - Standardise column names (snake_case)
   - Handle missing/invalid values (if any)
   - Convert types (ratings to numeric, IDs to int)
   - Feature engineering (examples):
     - `is_discounted`, `is_promo_used`
     - `spend_bucket` (low/medium/high)
     - `repeat_customer_flag` from previous purchases
     - `season_category` or `purchase_month` (if you derive dates later)

4. **SQL Analysis (PostgreSQL / MySQL / SQL Server)**
   - Load cleaned data into a table (e.g., `shopping_trends_clean`)
   - Create views for BI:
     - Spend by category / season / location
     - Promo vs non-promo performance
     - Subscription segmentation
     - Repeat purchase indicators

5. **Power BI Dashboard**
   - Connect Power BI to DB (preferred) or cleaned CSV
   - Build measures (Revenue, AOV proxy, Promo % share, Subscription share)
   - Publish dashboard visuals + slicers

6. **Report + Gamma PPT**
   - Business insights + evidence (charts + SQL outputs)
   - Actionable recommendations (marketing, retention, pricing/promos)

---

## Dashboard
**Power BI Dashboard Highlights**
- KPI Cards: Total Spend, Avg Spend, % Discounted, % Promo Used
- Spend by Category / Item Purchased
- Spend by Season + Subscription Status
- Payment Method & Preferred Payment Method comparison
- Repeat behaviour: Previous Purchases vs Spend / Rating
- Filters: Gender, Location, Season, Category, Subscription

> Add screenshots here: `reports/dashboard_screenshot.png`

---

## Results & Insights (Template)
Replace these with your real findings:
- **Top categories/items** driving spend and volume
- **Seasonal peaks** in purchase amount and category shifts
- **Promo/discount impact** (does it increase spend or just shift demand?)
- **Subscription effect** on frequency/previous purchases
- **Shipping + payment preferences** by segment (location/gender/age)

**Recommendations (examples)**
- Target promos to segments that show higher incremental spend (not everyone).
- Use subscription campaigns where repeat purchase signals are strongest.
- Optimise shipping options where they correlate with higher conversion/spend.

---
