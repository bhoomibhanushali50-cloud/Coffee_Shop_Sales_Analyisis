# ☕ Coffee Shop Sales Analysis
**Author:** Bhoomi Katarmal

An end-to-end Python data analytics project analysing a coffee shop's transactional sales data.

---

## 📂 Project Structure

```
CoffeShopProject/
├── Coffee_Shop_Sales.csv                  ← Raw dataset
├── BhoomiKatarmal_Coffee_Shop_Analysis.ipynb  ← Main analysis notebook
├── requirements.txt                       ← Python dependencies
└── README.md
```

---

## 📊 Analysis Covered

| Section | Description |
|---------|-------------|
| **1. Import Libraries** | pandas, numpy, matplotlib, seaborn |
| **2. Load & Inspect Data** | Shape, dtypes, missing values, unique values |
| **3. Data Cleaning & Feature Engineering** | Date parsing, revenue column, month/day/hour features |
| **4. EDA** | KPI summary, price/quantity/revenue distributions |
| **5. Sales Trend Analysis** | Monthly revenue, transaction trend, daily rolling average |
| **6. Product Analysis** | Top products by revenue & units, category share, avg price |
| **7. Store Performance** | KPIs per store, monthly comparison, stacked category bar |
| **8. Peak Hours & Day-of-Week** | Hourly dual-axis chart, day-of-week bars, heatmap |
| **9. Revenue Insights** | MoM growth, top-5 pie, revenue boxplot, qty-revenue scatter |
| **10. Findings & Recommendations** | Auto-generated summary + actionable business insights |

---

## 🚀 Quick Start

### 1 — Install dependencies
```bash
pip install -r requirements.txt
```

### 2 — Launch the notebook
```bash
jupyter notebook BhoomiKatarmal_Coffee_Shop_Analysis.ipynb
```

### 3 — Run all cells
In Jupyter: **Kernel → Restart & Run All**

---

## 🗂️ Dataset Columns

| Column | Description |
|--------|-------------|
| `transaction_id` | Unique transaction identifier |
| `transaction_date` | Date of transaction (MM/DD/YY) |
| `transaction_time` | Time of transaction (HH:MM:SS) |
| `transaction_qty` | Number of units purchased |
| `store_id` | Store identifier |
| `store_location` | Store name (Lower Manhattan, Hell's Kitchen, Astoria) |
| `product_id` | Product identifier |
| `unit_price` | Price per unit ($) |
| `product_category` | Category (Coffee, Tea, Bakery, etc.) |
| `product_type` | Specific product name |

---

## 📦 Dependencies

- `pandas` — data manipulation
- `numpy` — numerical operations
- `matplotlib` — base plotting
- `seaborn` — statistical visualisation
- `jupyter` / `notebook` — interactive environment

##DATA SOURCE
DATA SOURCED FROM Kaggle UNDER CC0 PUBLIC DOMAIN
