# Swiggy Sales Analytics & Dashboard

End-to-end food delivery sales analytics platform built on a large-scale operational dataset — combining a Microsoft Fabric data pipeline, SQL-based analysis, and an interactive Power BI dashboard to evaluate delivery fleet efficiency and revenue drivers.

---

## Business Problem

A food delivery platform generates enormous volumes of order-level data every day, but raw transaction logs don't answer the questions the business actually needs:

1. **Where is revenue actually coming from — which states, categories, and time windows drive the business?**
2. **How efficient is the delivery fleet, and where are the bottlenecks?**
3. **Are customers satisfied, and is order value trending in a healthy direction?**

This project turns 197K+ raw food delivery orders into a decision-ready analytics platform.

---

## Key Results

| Metric | Value |
|---|---|
| Orders analyzed | 197,000+ |
| Top-performing state | Karnataka — Rs. 5.5M in sales |
| Average Order Value (AOV) | Rs. 268.51 |
| Average customer rating | 4.34 / 5.0 |
| Peak ordering window | Weekend, peak hours |

**Core insight:** Sales are heavily concentrated by geography and time — Karnataka leads all states in revenue, and demand consistently spikes during weekend peak hours. This points directly to where fleet capacity and marketing spend should be prioritized.

---

## Tech Stack

- **Microsoft Fabric** — Lakehouse, Dataflow Gen2, Delta tables for the end-to-end data pipeline
- **SQL** — data cleaning, aggregation, and business logic
- **Power BI** — Power Query transformations, DAX measures, interactive dashboard
- **Python** — supporting data analysis and validation

---

## Project Workflow

```
Raw Order Data (197K+ records)
      │
      ▼
Microsoft Fabric Lakehouse  →  centralized storage layer
      │
      ▼
Dataflow Gen2  →  transformation & cleaning
      │
      ▼
Delta Tables  →  structured, query-ready data
      │
      ▼
SQL Analysis  →  revenue drivers, fleet efficiency, segmentation
      │
      ▼
Power BI Dashboard  →  Power Query + DAX measures  →  Interactive Reporting
```

1. **Ingestion & Storage (Microsoft Fabric):** Raw order data loaded into a Fabric Lakehouse, with Dataflow Gen2 handling transformation and Delta tables providing structured, queryable storage.
2. **Analysis (SQL & Python):** Delivery fleet efficiency and revenue drivers evaluated across geography, category, and time.
3. **Dashboard (Power BI):** Power Query used for shaping the data; DAX measures built to track sales, AOV, and satisfaction KPIs in real time.

---

## Dashboard Highlights

The Power BI dashboard surfaces:
- Revenue breakdown by state and category
- Order volume and peak-hour demand patterns
- Average Order Value and customer rating trends
- Delivery fleet efficiency metrics

*(Add a screenshot or GIF of the dashboard here — this is usually the first thing a recruiter or reviewer looks at.)*

```
![Dashboard Screenshot](assets/dashboard_preview.png)
```

---

## Repository Structure

```
├── data/                   # Raw and cleaned order datasets
├── fabric/                 # Dataflow Gen2 / Lakehouse pipeline artifacts
├── sql/                    # Analysis and transformation queries
├── notebooks/              # EDA and exploratory analysis
├── powerbi/                # .pbix dashboard file
├── assets/                 # Dashboard screenshots, charts
└── README.md
```

---

## How to Run

1. Clone the repository
   ```bash
   git clone https://github.com/mohitjain0810/Swiggy-Sales-Analyze-Project-And-Dashboard.git
   cd Swiggy-Sales-Analyze-Project-And-Dashboard
   ```
2. Set up the Microsoft Fabric Lakehouse and load the raw dataset from `/data`
3. Run the Dataflow Gen2 pipeline (or the SQL scripts in `/sql` if working from local CSVs)
4. Open `/powerbi/swiggy_sales_dashboard.pbix` in Power BI Desktop and point it to your data source

---

## Business Impact

This platform gives the business a single, reliable view of where sales are strongest, when demand peaks, and how satisfied customers are — enabling smarter decisions on fleet allocation, regional focus, and marketing timing instead of relying on gut feel or fragmented reports.

---

## Future Improvements

- Automate the Fabric pipeline refresh on a schedule
- Add a delivery-time / SLA breach analysis layer
- Extend the dashboard with a demand-forecasting model for peak-hour staffing

---

## Author

**Mohit Jain**
[LinkedIn](https://www.linkedin.com/in/mohit-jain-31bab7233/) · [Portfolio](https://mohitjaindataportfolio.netlify.app/) · [GitHub](https://github.com/mohitjain0810)
