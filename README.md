# NHS A&E Breach Risk Analysis

Analysis of 15 years of NHS England A&E performance data to identify 
breach risk patterns and understand why the 95% four-hour target has 
been missed 92% of the time.

---

```
nhs-ae-breach-risk/
│
├── nhs_ae_breach_risk.ipynb        # Full Python and SQL analysis
├── nhs_ae_clean.csv                # Cleaned dataset (15 years, monthly)
├── NHS_AE_Breach_Risk_Dashboard.pbix  # Power BI dashboard
├── requirements.txt                # Python dependencies
├── README.md                       # This file
│
└── outputs/
    ├── chart1_performance_trend.png
    ├── chart2_yearly_performance.png
    ├── chart3_seasonality.png
    └── chart4_gap_from_target.png
```

---

## Quick Start

1. Clone & install

git clone https://github.com/patilsuyog1994/nhs-ae-breach-risk.git
cd nhs-ae-breach-risk

pip install -r requirements.txt

2. Run the analysis

jupyter notebook nhs_ae_breach_risk.ipynb

---

## Dataset

Source: NHS England Open Data — england.nhs.uk

Column            | Type    | Description
------------------|---------|-----------------------------
period            | date    | Monthly reporting period
attendances       | int     | Total A&E attendances
seen_within_4hrs  | int     | Patients seen within 4 hours
performance_pct   | float   | % seen within 4-hour target
breach_gap        | float   | Gap from 95% target

---

## Methodology

**Data Cleaning** — raw NHS monthly CSVs parsed, column errors 
corrected, consistent date format applied across 15 years.

**SQL Analysis** — SQLite queries used to aggregate by year, month, 
and season to surface breach patterns.

**Visualisation** — matplotlib/seaborn charts built for trend, 
seasonality, yearly performance, and gap-from-target views.

**Dashboard** — Power BI report built on the cleaned CSV for 
interactive exploration.

---

## Key Findings

- NHS missed the 95% target in 169 out of 184 months (92% of the time)
- 2022 was the worst year on record — only 57.6% seen within 4 hours
- Winter months (December, January, February) consistently underperform
- Performance has not recovered since COVID-19

---

## Dependencies

Package       | Purpose
--------------|-------------------------
pandas        | Data manipulation
matplotlib    | Visualisation
seaborn       | Statistical charts
sqlite3       | SQL querying

---

## Author

Suyog Patil

Data Analyst — Sheffield, UK

github.com/patilsuyog1994
