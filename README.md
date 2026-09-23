# ☕ Coffee Shop Sales Analysis
**Author:** Bhoomi Katarmal  
**Dataset:** `Coffee_Shop_Sales.csv`  
**Status:** ✅ Finalised — June 2025

An end-to-end Python data analytics project analysing a coffee shop chain's transactional sales data, with an interactive Streamlit web dashboard.

---

## 📂 Project Structure

```
CoffeShopProject/
├── Coffee_Shop_Sales.csv       ← Raw dataset (149,116 records)
├── streamlit_app.py            ← Interactive Streamlit dashboard
├── charts/                     ← Exported PNG chart images (18 files)
│   ├── 01_eda_distributions.png
│   ├── 02_monthly_revenue.png
│   ├── 03_monthly_transactions.png
│   ├── 04_daily_revenue_rolling.png
│   ├── 05_product_category.png
│   ├── 06_top10_by_revenue.png
│   ├── 07_top10_by_units.png
│   ├── 08_avg_unit_price.png
│   ├── 09_store_kpis.png
│   ├── 10_store_monthly.png
│   ├── 11_store_category_stacked.png
│   ├── 12_hourly_dual_axis.png
│   ├── 13_day_of_week.png
│   ├── 14_heatmap.png
│   ├── 15_mom_growth.png
│   ├── 16_top5_pie.png
│   ├── 17_revenue_boxplot.png
│   └── 18_qty_revenue_scatter.png
└── README.md
```

---

## 📊 Analysis Covered

| # | Section | Description |
|---|---------|-------------|
| 1 | **Load & Inspect Dataset** | Shape, dtypes, sample rows, column overview |
| 2 | **Data Quality Check** | Missing values, duplicates, invalid numeric detection |
| 3 | **Feature Engineering** | `total_sales = qty × unit_price`, date/time parsing, derived columns |
| 4 | **Group & Summarise** | KPI summary, by-category, by-store, monthly aggregations |
| 5 | **Sales Trend Analysis** | Monthly revenue bar+line, transaction count, 7-day rolling average |
| 6 | **Product Analysis** | Revenue pie, top-10 by revenue & units, avg price by category |
| 7 | **Store Performance** | KPI comparison, monthly by-store line, stacked category bar |
| 8 | **Peak Hours & Day-of-Week** | Dual-axis hourly chart, day-of-week bars, transaction heatmap |
| 9 | **Revenue Insights & MoM** | MoM growth bar, top-5 pie, revenue boxplot, qty-revenue scatter |
| 10 | **Business Recommendations** | Auto-generated final summary + 6 actionable insights |

---

## 🚀 Quick Start — Streamlit Dashboard

### Step 1 — Install Python dependencies

```powershell
& "$env:LOCALAPPDATA\Programs\Python\Python314\python.exe" -m pip install pandas numpy matplotlib seaborn streamlit
```

### Step 2 — Launch the dashboard

```powershell
cd "C:\Users\Admin\Downloads\CoffeShopProject"
& "$env:LOCALAPPDATA\Programs\Python\Python314\python.exe" -m streamlit run streamlit_app.py
```

### Step 3 — Open in browser

Dashboard auto-opens at **http://localhost:8501**

---

## 🌐 Streamlit Dashboard Features

| Feature | Details |
|---------|---------|
| **Sidebar Filters** | Store location, Product category, Month multi-select |
| **KPI Cards** | Total Revenue, Transactions, Avg Order Value, Units Sold, Products, Stores |
| **Data Quality Check** | Missing values, duplicates, raw data preview, column info |
| **Sales Trends** | Tabbed view — Monthly revenue, Transaction count, Daily rolling avg |
| **Product Analysis** | Revenue pie, category bars, Top-10 revenue & units charts |
| **Store Comparison** | KPI bars, monthly revenue line chart by store |
| **Peak Hours** | Dual-axis hourly chart, Day-of-week bars, Transaction heatmap |
| **Revenue Insights** | MoM growth bar, Top-5 products pie, Revenue boxplot |
| **Recommendations** | Auto-generated key findings + 6 colour-coded business recommendations |

---

## 🗂️ Dataset Columns

| Column | Type | Description |
|--------|------|-------------|
| `transaction_id` | int | Unique transaction identifier |
| `transaction_date` | date | Date of transaction (MM/DD/YY) |
| `transaction_time` | time | Time of transaction (HH:MM:SS) |
| `transaction_qty` | int | Number of units purchased |
| `store_id` | int | Store identifier |
| `store_location` | str | Store name (Lower Manhattan, Hell's Kitchen, Astoria) |
| `product_id` | int | Product identifier |
| `unit_price` | float | Price per unit ($) |
| `product_category` | str | Category (Coffee, Tea, Bakery, etc.) |
| `product_type` | str | Specific product name |
| `total_sales` *(derived)* | float | `transaction_qty × unit_price` |

---

## 📦 Dependencies

| Package | Version | Purpose |
|---------|---------|---------|
| `pandas` | ≥ 2.0.0 | Data loading, cleaning, aggregation |
| `numpy` | ≥ 1.24.0 | Numerical operations |
| `matplotlib` | ≥ 3.7.0 | Base charting & axis formatting |
| `seaborn` | ≥ 0.12.0 | Statistical visualisation & heatmaps |
| `streamlit` | ≥ 1.28.0 | Interactive web dashboard |

Install all at once:
```powershell
& "$env:LOCALAPPDATA\Programs\Python\Python314\python.exe" -m pip install pandas numpy matplotlib seaborn streamlit
```

---

## 📈 Key Results

| KPI | Value |
|-----|-------|
| Total Revenue | **$698,812.33** |
| Total Transactions | **149,116** |
| Avg Transaction Value | **$4.69** |
| Total Units Sold | **214,470** |
| Best Month | **June** |
| Best Store | **Hell's Kitchen** |
| Best Product | **Barista Espresso** |
| Peak Hour | **10:00 – 11:00** |
| Busiest Day | **Friday** |

---

## 💡 Key Findings & Recommendations

### Findings
1. Revenue grew **consistently month-over-month** from January to June, peaking in June ($166,485).
2. **Coffee** is the dominant category (~39% revenue share), followed by Tea (~28%).
3. All three stores (**Lower Manhattan, Hell's Kitchen, Astoria**) perform comparably (~33% each).
4. **Peak hours** are 8 AM – 11 AM, driven by morning commuter traffic.
5. **Weekdays** (especially Friday) significantly outperform weekends in transactions.
6. **Barista Espresso** and **Brewed Chai Tea** are the top revenue-generating products.

### Recommendations
1. **Off-peak promotions** — happy-hour deals (2–5 PM) to capture afternoon footfall.
2. **Weekend bundles** — pastry + coffee combos to close the weekday–weekend gap.
3. **Seasonal variants** — iced espresso (summer) / spiced chai (autumn) to sustain demand.
4. **SKU rationalisation** — review Packaged Chocolate & Branded items; replace with higher-demand products.
5. **Inventory planning** — stock espresso beans & chai concentrate before 8 AM peak.
6. **Loyalty programme** — high repeat volume suggests a points-based rewards system would boost retention.

---

*Coffee Shop Sales Analysis — Bhoomi Katarmal — June 2025*
