<div align="center">

# 📊 Data Science Internship — Week 1 Assignment

### Data Cleaning, Sales Analysis & Visualization

<img src="https://img.shields.io/badge/Organization-WeIntern%20Pvt%20Ltd-2563EB?style=for-the-badge">
<img src="https://img.shields.io/badge/Domain-Data%20Science-EA580C?style=for-the-badge">
<img src="https://img.shields.io/badge/Focus-EDA%20%26%20Visualization-16A34A?style=for-the-badge">
<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge">

**Week 1**

</div>

---

## Table of Contents

- [Objective](#objective)
- [Dataset Description](#dataset-description)
- [Tools and Libraries](#tools-and-libraries)
- [Key Steps Performed](#key-steps-performed)
- [Major Findings](#major-findings)
- [Folder Structure](#folder-structure)
- [Execution Instructions](#execution-instructions)
- [Author](#author)

---

## Objective

Build disciplined habits in data cleaning, structured analysis, exploratory thinking, visualization, and professional reporting using a real-world style e-commerce dataset.

---

## Dataset Description

| Attribute | Detail |
|-----------|--------|
| **File** | `data/raw/ecommerce_raw.csv` |
| **Rows** | 1,015 (including duplicates and intentional data quality issues) |
| **Columns** | 11 |
| **Fields** | Order ID, Customer ID, Product Name, Category, Quantity, Unit Price, Total Amount, Order Date, Payment Mode, Delivery Status, City |
| **Period** | January 2024 – December 2024 |
| **Intentional quality issues** | ~140 missing values, 15 duplicate rows, 8 invalid quantities, 5 zero prices, 6 unparseable dates, 8 inconsistent category spellings |

---

## Tools and Libraries

<div align="center">

<img src="https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white">
<img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white">
<img src="https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge">
<img src="https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge">
<img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white">

</div>

| Library | Version | Purpose |
|---------|---------|---------|
| pandas | 2.2.2 | Data loading, cleaning, grouping |
| numpy | 1.26.4 | Numeric operations |
| matplotlib | 3.9.0 | All charts and dashboard |
| seaborn | 0.13.2 | Supporting visualizations |
| jupyter | 1.0.0 | Notebook environment |

---

## Key Steps Performed

### Task 1 — Data Cleaning

- Detected and removed 15 fully duplicated rows
- Dropped 6 rows with unparseable Order Date values
- Standardised 8 inconsistent Category spellings (e.g. `electronics` → `Electronics`)
- Replaced 8 invalid (negative/zero) Quantity values with NaN → filled with median
- Replaced 5 zero Unit Price values → filled with category-wise median
- Filled missing City with `Unknown`, Payment Mode and Delivery Status with column mode
- Filled missing Product Name with `Unknown Product`
- Recalculated Total Amount after all numeric corrections
- **Final cleaned dataset: 994 rows, 0 nulls**

### Task 2 — Sales Analysis

- Computed 7 core KPIs: Total Revenue, Total Orders, AOV, Units Sold, Top Category, Best Product, Repeat Rate
- Monthly trend analysis with MoM growth calculation
- Category-wise performance breakdown
- City-level sales concentration analysis
- Customer behaviour: repeat vs. single-order buyers
- Delivery status impact on realized revenue

### Task 3 — Visualizations

- 7 individual charts (bar, line, pie) with full labels and written findings
- 1 full dashboard mockup (KPI cards + 4 panels)
- All charts saved to `outputs/charts/` and `outputs/dashboard/`

---

## Major Findings

1. **Electronics** is the highest-revenue category, driven by premium unit prices
2. Sales **peak in the second half of the year** (festive season effect)
3. **Mumbai, Delhi, Bengaluru** account for ~45% of orders
4. **~65% of customers are repeat buyers** — retention is the key growth lever
5. **~15% of orders are cancelled or returned** — a logistics/quality risk
6. **UPI + Credit Card** dominate payments (>55% combined share)

---

## Folder Structure

```
data-science-week1-assignment/
├── data/
│   ├── raw/
│   │   └── ecommerce_raw.csv          # Original dataset (never modified)
│   └── cleaned/
│       └── ecommerce_cleaned.csv      # Output of Task 1
├── notebooks/
│   └── week1_analysis.ipynb           # Main analysis notebook (Tasks 1–3)
├── outputs/
│   ├── charts/
│   │   ├── 01_revenue_by_category.png
│   │   ├── 02_orders_by_city.png
│   │   ├── 03_top10_products_units.png
│   │   ├── 04_monthly_sales_trend.png
│   │   ├── 05_category_monthly_trend.png
│   │   ├── 06_payment_mode_pie.png
│   │   └── 07_delivery_status_pie.png
│   └── dashboard/
│       └── dashboard_mockup.png       # Full KPI dashboard
├── reports/
│   └── final_report.md                # Structured written report
├── screenshots/                       # (Add notebook screenshots here)
├── README.md
└── requirements.txt
```

---

## Execution Instructions

```bash
# 1. Clone or extract the project
cd data-science-week1-assignment

# 2. Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate        # Mac/Linux
venv\Scripts\activate           # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch Jupyter Notebook
jupyter notebook

# 5. Open and run the notebook
# File: notebooks/week1_analysis.ipynb
# Run All Cells (Kernel → Restart & Run All)
```

> **Note:** Run all cells from top to bottom in order. The notebook is self-contained — it generates the cleaned dataset and all chart outputs automatically.

---

## Author

| | |
|---|---|
| **Name** | Akshat Singh |
| **Internship** | Data Science — WeIntern Pvt Ltd |
| **Week** | 1 |
| **Date** | 8 June 2024 |
