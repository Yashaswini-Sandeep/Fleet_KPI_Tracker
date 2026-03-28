readme_content = """# Vessel Fleet Performance KPI Tracker

A Python-based fleet analytics project simulating the day-to-day work of a
Fleet Analytics & Performance team — covering multi-source data integration,
KPI monitoring, anomaly detection, and financial impact quantification.

---

## Business Context

Shipping companies like Hapag-Lloyd operate large fleets across global routes.
Fleet performance data arrives from multiple internal systems — vessel operations,
commercial finance, and maintenance — and must be reconciled before analysis.
Identifying underperforming voyages early and quantifying their financial impact
is critical to cost control and operational efficiency.

This project simulates that end-to-end workflow using real-world ship performance
data sourced from Kaggle.

---

## Project Highlights

- **Multi-source data pipeline**: Dataset split into three departmental source
  files (Operations, Finance, Maintenance) and merged on a unique Voyage ID,
  simulating real ERP and system integration
- **Data reconciliation**: 609 incomplete records identified, flagged, and handled
  transparently without data loss
- **KPI monitoring**: Fleet-wide benchmarks computed across speed, fuel efficiency,
  operational cost, revenue, cargo load, and turnaround time
- **Anomaly detection**: Z-score method (threshold 1.5) applied across three KPIs.
  975 anomalous voyages detected, representing a 35.64% anomaly rate
- **ROI analysis**: Estimated $103.9M annual financial impact if anomalies remain
  unresolved, broken down into excess operational cost and lost revenue
- **Interactive dashboard**: Six-panel Plotly dashboard saved as a standalone HTML file
- **Management report**: Four-sheet Excel report with executive summary, monthly
  trends, anomaly log, and route and ship type performance breakdown

---

## Key Findings

| KPI | Value | Status |
|-----|-------|--------|
| Average Speed | 17.6 knots | Normal |
| Fuel Efficiency | 0.7987 nm/kWh | Normal |
| Avg Operational Cost | $255,143 | Normal |
| Avg Revenue per Voyage | $521,362 | Normal |
| Avg Cargo Load | 75.22% | Normal |
| Anomaly Rate | 35.64% | Warning |

Tankers show the highest anomaly rate at 38.57%, with Speed Deviation (31%)
and Low Efficiency (28.9%) as the dominant anomaly types across the fleet.

Resolving detected anomalies represents an estimated **$103.9M annual saving
opportunity** for the fleet.

---

## Dataset

- **Source**: [Ship Performance Clustering Dataset — Kaggle](https://www.kaggle.com/datasets/jeleeladekunlefijabi/ship-performance-clustering-dataset)
- **Records**: 2,736 voyages across 4 ship types
- **Period**: June 2023 – June 2024
- **Ship types**: Container Ship, Bulk Carrier, Tanker, Fish Carrier
- **Routes**: Coastal, Short-haul, Long-haul, Transoceanic

---

## Project Structure
```
Fleet_KPI_Tracker/
│
├── data/
│   ├── Ship_Performance_Dataset.csv     <- Original Kaggle dataset
│   ├── source_operations.csv            <- Simulated Operations system feed
│   ├── source_finance.csv               <- Simulated Finance system feed
│   └── source_maintenance.csv           <- Simulated Maintenance system feed
│
├── notebooks/
│   └── Fleet_KPI_Analysis.ipynb         <- Full analysis notebook
│
├── outputs/
│   ├── fleet_kpi_report.xlsx            <- Excel management report (4 sheets)
│   └── anomaly_summary.csv              <- Flagged voyage records
│
├── dashboard/
│   └── fleet_dashboard.html             <- Interactive Plotly dashboard
│
└── README.md
```

---

## Tools and Libraries

- **Python**: Pandas, NumPy, SciPy, Plotly, OpenPyXL
- **Analysis**: Z-score anomaly detection, multi-source data merging, KPI benchmarking
- **Reporting**: Interactive HTML dashboard, formatted Excel workbook
- **Version control**: Git / GitHub

---

## How to Run

1. Clone the repository
2. Install dependencies: `pip install pandas numpy scipy plotly openpyxl kaleido`
3. Place `Ship_Performance_Dataset.csv` in the `data/` folder
4. Open and run `notebooks/Fleet_KPI_Analysis.ipynb` from top to bottom
5. View dashboard: open `dashboard/fleet_dashboard.html` in any browser
6. View report: open `outputs/fleet_kpi_report.xlsx`
"""

with open('../README.md', 'w', encoding='utf-8') as f:
    f.write(readme_content)

print("README.md written successfully.")