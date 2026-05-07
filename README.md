# 📊 Sales Analytics Dashboard — Sample Superstore

> An end-to-end Excel analytics project built on the Sample Superstore dataset, covering customer segmentation, RFM analysis, churn tracking, profitability deep-dives, and fulfilment performance — all surfaced through a multi-page interactive dashboard.

---

## 🗂️ Project Structure

| Sheet | Purpose |
|---|---|
| `Sample - Superstore` | Raw transactional data (9,994 rows, 28 columns) — the single source of truth |
| `Pivots` | Underlying PivotTables powering all dashboard metrics |
| `DashboardMetrics` | KPI cards: total sales, profit, cost, fulfilment period, top products, top customers |
| `DashboardGraphs` | Visual pages 1–4: trend charts, regional breakdowns, category analysis |
| `DashboardGraphs2` | Customer analytics: total customers, retention rate, RFM segmentation |

---

## 📐 Dataset Overview

- **Period:** 2014–2017
- **Rows:** 9,994 order lines across 5,009 unique orders
- **Customers:** 793 unique customers
- **Columns include:** Order & ship dates, ship mode, customer segment, region, product category/sub-category, sales, cost, discount, profit, and 6 engineered features (fulfilment period, order quarter, ship quarter, day-of-week flags, year)

---

## 🔑 Key Findings

### 💰 Revenue & Profitability

| Metric | Value |
|---|---|
| Total Sales (all years) | $2,297,201 |
| Total Profit | $286,397 |
| Total Cost | $2,010,804 |
| Overall Profit Margin | **12.5%** |

- Sales grew consistently year-on-year: **$484K (2014) → $733K (2017)** — a 51% increase over the period.
- Profit followed the same trajectory: **$49.5K → $93.4K**, nearly doubling between 2014 and 2017.
- **West** is the highest-revenue region ($725K), with **East** close behind ($679K). **South** trails at $392K.

---

### 🏷️ Category Performance

| Category | Profit Margin |
|---|---|
| Technology | 17.4% |
| Office Supplies | 17.0% |
| **Furniture** | **2.5%** |

- **Technology and Office Supplies** are the profit engines of the business.
- **Furniture is a red flag** — despite being a significant revenue contributor, it generates only a 2.5% margin, dragged down heavily by Tables (-$17,725 total profit) and Bookcases (-$3,473).
- **Copiers** are the single most profitable sub-category ($55,618), followed by Phones ($44,516) and Accessories ($41,937).

---

### 🔻 The Discount Problem

| Cohort | Avg Profit per Line |
|---|---|
| No discount | **$66.90** |
| Discount applied | **-$6.66** |

- Over **5,196 out of 9,994 order lines (52%)** carried a discount.
- Discounted orders are on average **loss-making**. This is the single biggest profitability lever in the dataset.
- Heavy discounting on already low-margin categories (Furniture, Binders, Machines) is destroying value.

---

### 👥 Customer Analytics

| Metric | Value |
|---|---|
| Total Customers (2016 filtered) | 638 |
| Retained Customers | 452 (70.8%) |
| At Risk | 121 |
| Churned | 23 |
| Champions | 112 |
| Loyal | 367 |
| Hibernating | 239 |
| Big Spenders | 97 |

- **Retention rate of ~71%** is a healthy baseline, but the **239 hibernating customers** represent a significant re-engagement opportunity.
- **Top customer by profit:** Christopher Martinez (CM-12385) — $3,197 profit contribution.
- The **RFM segmentation** (Champions, Loyal, At Risk, Hibernating, Big Spenders) provides a structured basis for targeted marketing and retention campaigns.

---

### 🚚 Fulfilment Performance

- **Average fulfilment period: 4.0 days** across all orders.
- Standard Class accounts for ~60% of all orders — the dominant ship mode.
- Same Day shipping (543 orders) suggests a premium service tier exists but is used sparingly.

---

### 📅 Seasonal Patterns

- **Q4 is consistently the strongest quarter** for both sales and profit across all years — typical retail seasonality.
- Q1 (January in particular) regularly sees negative or near-zero profit, indicating post-holiday demand slumps or markdown pressure.

---

## 🛠️ Technical Implementation

- **Platform:** Microsoft Excel (.xlsm with macro support)
- **Data Modelling:** PivotTables with calculated fields for profit margin, fulfilment period, RFM segment classification
- **Customer Segmentation:** RFM logic (Recency, Frequency, Monetary) implemented via PivotTable-derived segments
- **Churn Analysis:** Year-over-year customer cohort comparison — retained, new, at-risk, and churned cohorts tracked
- **Dashboard Design:** Multi-page layout with KPI cards, slicers, and chart pages (DashboardGraphs / DashboardGraphs2)
- **Engineered Features:** `FulfilmentPeriod`, `OrderQuarter`, `ShipQuarter`, `OrderDayOfWeek`, `IsWeekend`, `Year` — all derived from raw date fields to enable time-based analysis

---

## 💡 Business Recommendations

1. **Audit the discount strategy** — over half of all transactions are discounted and unprofitable on average. A tiered discount cap policy would meaningfully improve margins.
2. **Investigate Furniture sub-categories** — Tables and Bookcases are consistently loss-making. Either reprice, renegotiate supplier costs, or deprioritise heavy-discount Furniture SKUs.
3. **Re-engage hibernating customers** — 239 customers who have gone quiet are a warm audience. Targeted outreach with personalised offers based on their historical purchase category is a low-cost growth lever.
4. **Double down on Technology** — highest margin category with consistent growth. Copiers and Phones should be the focus of upsell and cross-sell activity.
5. **Leverage Q4 seasonality** — the data clearly shows Q4 outperformance. Marketing and inventory investment should be front-loaded into Q3 to capitalise on this.

---

## 📁 Files

| File | Description |
|---|---|
| `Sales_Analytics.xlsm` | Main workbook — data, pivots, and full dashboard |

---

## 👤 Author

**Aashish** — MEng Computer Systems Engineering  
Data Analyst Portfolio Project  
[GitHub Profile](https://github.com/)
