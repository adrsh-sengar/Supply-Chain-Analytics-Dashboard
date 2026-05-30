# Supply Chain Management Dashboard

A data analytics project built to solve a real operational problem — when a business has no centralised visibility into its supply chain, decisions get made on gut feeling rather than data. This dashboard changes that.

---

## The Problem

Most supply chain teams track things in scattered spreadsheets — delivery status in one file, inventory levels in another, supplier performance somewhere else entirely. There's no single place to look when something goes wrong, and by the time someone spots a problem, it's already cost the business time and money.

This project builds that single source of truth.

---

## What I Built

An end-to-end supply chain analytics pipeline and Power BI dashboard for an automotive company, covering:

- **Delivery Performance** — on-time delivery rate, delays by route and supplier
- **Inventory Tracking** — stock levels, inventory turnover, production schedule adherence
- **Supplier Quality** — vendor-wise quality scores, defect rates, procurement risk indicators

The dashboard lets operations and procurement teams filter by supplier, time period, and product category — so instead of pulling 3 reports and combining them manually, the answer is one click away.

# Supply Chain Management Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/8d42a5e4-9ebd-46c7-bf6a-a66f2648c422/ReportSection?experience=power-bi

---

## Tools Used

- **Python** — data ingestion from Kaggle API, cleaning and loading into SQL Server
- **MS SQL Server** — structured storage, SQL queries for KPI calculation and root cause analysis
- **Power BI** — multi-page interactive dashboard (Star Schema data model, DAX measures, slicers, drill-throughs)

---

## How It Works

**Step 1 — Data Ingestion**
Python pulls the raw automotive supply chain dataset via the Kaggle API and loads it into MS SQL Server after basic cleaning and validation. This replaces any manual CSV download and upload process.

**Step 2 — Data Modelling**
Inside SQL Server, the data is structured into fact and dimension tables (Star Schema). SQL queries extract KPIs like on-time delivery %, average lead time, and supplier defect rate.

**Step 3 — Dashboard**
Power BI connects to SQL Server and visualises everything across two main pages:
- Page 1: Delivery and production performance
- Page 2: Supplier quality and inventory levels

DAX measures are used for dynamic KPI calculations that respond to slicer selections.

---

## Key Findings

- Identified vendor-level quality gaps that were previously invisible in spreadsheet-based reporting
- Surfaced which suppliers consistently underperformed on delivery timelines
- Highlighted inventory bottlenecks tied to specific production schedules
- Enabled the procurement team to prioritise vendor reviews based on actual data rather than assumptions

---

## What I Learned

Building this made me realise how much operational data already exists inside most businesses — it just isn't connected. The real skill isn't in making a pretty dashboard; it's in understanding the business problem first, then figuring out which data answers it and how to structure that data so the dashboard actually makes sense to someone who uses it every day.

SQL-based root cause analysis was particularly useful here — being able to drill into supplier quality at a granular level and surface patterns that aggregate views would miss.

---

## File Structure

```
├── data/                  # Raw dataset files
├── sql/                   # SQL queries for KPI extraction
├── python/                # Python scripts for data ingestion and cleaning
├── dashboard/             # Power BI .pbix file
└── README.md
```

---

## How to Run

1. Clone this repository
2. Run the Python script in `/python/` to load data into your local SQL Server instance
3. Open the `.pbix` file in Power BI Desktop
4. Update the data source connection to point to your SQL Server
5. Refresh — the dashboard loads with your data
---

*Built by Adarsh Sengar | B.Tech, Punjab Engineering College, Chandigarh*
