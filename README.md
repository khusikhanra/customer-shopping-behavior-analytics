<div align="center">

# 🛍️ Customer Shopping Behavior Analytics

**An end-to-end retail analytics project uncovering spend patterns, loyalty gaps, and promo adoption opportunities across 3,900 customers.**

[![Made with Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![SQL](https://img.shields.io/badge/SQL-Analysis-336791?style=flat-square&logo=postgresql&logoColor=white)]()
[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=flat-square&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-00B4D8?style=flat-square)](LICENSE)
[![Dataset](https://img.shields.io/badge/Dataset-3%2C900%20Records-8DA5C0?style=flat-square)]()

</div>

<div align="center">

![Dashboard Preview](assets/dashboard-preview.png)

</div>

---

## 📌 Project Overview

Retail businesses generate massive volumes of transactional data — but raw data alone doesn't drive decisions. This project transforms a 3,900-record customer dataset into a fully actionable analytics pipeline, spanning data exploration, SQL-based segmentation, Power BI reporting, and an interactive browser dashboard.

The central question driving this work:

> *Where are the highest-value customers, what drives their spend, and where is revenue being left on the table?*

The answer surfaces a striking promo adoption gap — **subscribers use promo codes 100% of the time; non-subscribers use them 0%** — representing a potential **~$1.2M in untapped GMV** from conversion alone.

---

## 📁 Repository Structure

```
customer-shopping-behavior-analytics/
│
├── 📂 data/
│   └── Customer_Shopping_Behavior_Analysis.xlsx             # Raw dataset — 3,900 rows, 18 variables
│
├── 📂 sql/
│   └── analysis_queries.sql                                 # KPIs, segmentation, cohort & promo queries
│
├── 📂 python/
│   └── eda_analysis.py                                      # Data cleaning, EDA, and aggregation scripts
│
├── 📂 dashboard/
│   └── Customer_Shopping_Dashboard.html                     # Self-contained interactive HTML dashboard
│
├── 📂 powerbi/
│   ├── Customer_Shopping_Behavior_Analysis_Dashboard.pbix   # Power BI report file
│   └── README.md                                            # Power BI setup and report guide
│
├── 📂 presentation/
│   └── Customer_Shopping_Behavior_Analysis.pptx             # Executive presentation deck
│
├── 📂 assets/
│   └── dashboard-preview.png                                # Dashboard screenshot for README
│
├── .gitignore
├── LICENSE
└── README.md
```

---

## 📊 Dataset at a Glance

| Variable | Detail |
|---|---|
| **Records** | 3,900 customers |
| **Variables** | 18 features |
| **Age Range** | 18 – 70 years (avg 44.1) |
| **Geographies** | 50 unique US locations |
| **Categories** | Clothing · Accessories · Footwear · Outerwear |
| **Products** | 25 unique items |
| **Seasons** | Spring · Summer · Fall · Winter |
| **Payment Methods** | PayPal · Credit Card · Cash · Debit Card · Venmo · Bank Transfer |
| **Shipping Types** | 6 options including Free, Express, Next Day Air |

---

## 🔍 Key Findings

### 💰 Revenue & Spend
- Average order value: **$59.76** across all segments
- **Footwear** has the highest avg spend at **$60.26** despite being 3rd in volume
- **18–30 age group** outspends all others at **$60.39 avg** — the highest-value demographic
- **31–45** is the lowest at **$59.40** — a segment worth re-engaging

### 👥 Customer Segments
- **68% Male** (2,652) vs **32% Female** (1,248)
- **27% are subscribers** (1,053 customers), **73% non-subscribers** (2,847)
- Avg previous purchases per customer: **25.4 orders**

### ⚡ The Promo Gap — Biggest Insight
| Segment | Promo Usage | Customers |
|---|---|---|
| Subscribers | **100%** | 1,053 |
| Non-Subscribers | **0%** | 2,847 |

Converting just **10% of non-subscribers** to promo users = **~$1.2M in untapped GMV**

### 🗓️ Seasonality & Purchase Frequency
- Spend is nearly **flat across all 4 seasons** (Spring leads at 999 customers)
- Purchase frequency is **evenly distributed** — no single cadence dominates
- Suggests strong habitual buying behavior rather than seasonal spikes

---

## 🛠️ Tools & Tech Stack

| Layer | Tool | Purpose |
|---|---|---|
| **Data Storage** | Microsoft Excel (.xlsx) | Raw dataset source |
| **Data Analysis** | Python 3.11 · pandas · numpy | Cleaning, EDA, aggregations |
| **SQL Analysis** | Standard SQL (PostgreSQL-compatible) | Segmentation, KPIs, cohort queries |
| **BI Reporting** | Microsoft Power BI | Executive-level visual reporting |
| **Web Dashboard** | Vanilla HTML · CSS · SVG | Self-contained interactive dashboard |

---

## 🖥️ Interactive Dashboard

A fully self-contained HTML dashboard — **no frameworks, no CDN, no build step** — that opens directly in Chrome.

**Features:**
- 8 animated SVG charts (bars, donuts, heatmaps)
- 4 KPI cards with count-up animation and sparklines
- Live filter panel (Season · Category · Gender · Subscription) — all 8 charts recompute in real time
- Cursor-following tooltips on every element
- Promo insight banner with GMV opportunity callout
- Live clock in header

**To open:** Download `dashboard/Customer_Shopping_Dashboard.html` → open in Chrome. No server needed.

---

## 🗄️ SQL Analysis

Queries in `sql/analysis_queries.sql` cover:

- **KPI Summary** — total customers, avg order value, avg rating, subscriber rate
- **Category Performance** — avg spend, order volume, revenue share by category
- **Demographic Segmentation** — spend by age group and gender
- **Seasonal Analysis** — transaction volume and avg spend by season
- **Payment & Shipping Breakdown** — ranked by usage
- **Promo & Discount Cohort** — subscriber vs non-subscriber behavior
- **Purchase Frequency Distribution** — cadence analysis
- **High-Value Customer Identification** — top spenders by previous purchase history

---

## 🐍 Python EDA

`python/eda_analysis.py` covers:

- Data loading and schema validation
- Missing value detection and handling
- Outlier analysis on purchase amounts and ratings
- Distribution plots for age, spend, and rating
- Correlation heatmap across numerical variables
- Aggregation exports used for dashboard and Power BI

---

## 📈 Power BI Report

The Power BI report file (`powerbi/Customer_Shopping_Behavior_Analysis_Dashboard.pbix`) can be opened directly in Power BI Desktop.

The report includes:
- Executive summary page with KPI cards
- Category and seasonal performance views
- Subscriber vs non-subscriber deep dive
- Demographic breakdown (age, gender, geography)
- Promo adoption funnel

---

## 📑 Presentation

The executive presentation (`presentation/Customer_Shopping_Behavior_Analysis.pptx`) summarises all key findings in a stakeholder-ready format — designed for business reviews, portfolio showcases, and client-facing demos.

Covers: project overview · dataset summary · key findings · promo gap insight · recommendations · next steps.

---

## 🚀 Getting Started

**1. Clone the repo**
```bash
git clone https://github.com/khusikhanra/customer-shopping-behavior-analytics.git
cd customer-shopping-behavior-analytics
```

**2. Set up Python environment**
```bash
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install pandas numpy matplotlib seaborn openpyxl
```

**3. Run the EDA script**
```bash
python python/eda_analysis.py
```

**4. Open the dashboard**
```bash
# Just open in Chrome — no server needed
open dashboard/Customer_Shopping_Dashboard.html
```

**5. Run SQL queries**
Import `data/Customer_Shopping_Behavior_Analysis.xlsx` into your database of choice and run `sql/analysis_queries.sql`.

---

## 📌 Potential Next Steps

- [ ] **Customer Churn Prediction** to identify at-risk accounts and improve retention
- [ ] **Customer Lifetime Value (LTV) Modeling** to prioritize high-value customer segments
- [ ] **Subscription Conversion Funnel Analysis** to uncover drop-off points and improve trial-to-paid conversion
- [ ] **Cohort Retention Analysis** to measure long-term customer engagement and product stickiness
- [ ] **Revenue Forecasting Model** to support growth planning and ARR projections
- [ ] **Product Usage Segmentation** to identify power users, expansion opportunities, and upsell candidates
- [ ] **SaaS KPI Executive Dashboard** covering MRR, ARR, Retention, Churn, LTV, CAC, and Expansion Revenue

---

## 👤 Author

**Khusi Khanra**
Data Driven Consultant

[![GitHub](https://img.shields.io/badge/GitHub-khusikhanra-181717?style=flat-square&logo=github)](https://github.com/khusikhanra)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

<div align="center">
<sub>Built with 🔍 curiosity and ☕ coffee · Dataset: 3,900 customers · 18 variables</sub>
</div>

