# Logistics Cost Optimization

## **Project Overview**

**The Chaos on the Ground:** A global logistics team lacked deep visibility into shipment reliability and true cost efficiency. Delays were frequent, and isolating the root causes of supply chain friction was heavily reliant on manual spreadsheet analysis, leading to expensive blind spots.
**The Solution:** I engineered a programmatic "Control Tower" using Python for data engineering and Tableau for visualization. I conducted variance analysis on shipment and logistics data to identify that two product groups accounted for over 99% of total logistics spend. I also built interactive Tableau dashboards to support supply chain demand planning and strategic vendor management decisions.

## **Data Sources**

- **SCMS Delivery History Exports (`SCMS_Delivery_History_Dataset.csv`):** Historical shipment data tracking vendors, freight costs, and delivery dates across multiple complex routes.

## **Process**

- **Data Engineering (Python/Pandas):** Replaced manual data cleansing with robust Python scripts to handle missing capture dates, impute NULLs for critical fields like "Shipment Modes", and standardize Weight/Freight conversions for flawless aggregation.
- **KPI Programmatic Logic:** Engineered strict logic to calculate key KPIs, including on-time delivery (OTD), lead time variance, and freight-cost-to-value ratios to evaluate vendor capabilities and logistics performance.
- **Interactive Control Tower:** Deployed Tableau dashboards with dynamic filters, enabling real-time, ad-hoc exploration of supply network friction.

## **Key Findings**

- **Cost Concentration:** Discovered that ARV and HRDT product groups account for **99% of total logistics spend** (over $1.46B+), instantly highlighting where to focus cost-saving negotiations.
- **Mode Reliability & Variance:** Identified an **88.5% overall OTD rate**, noting that Ocean shipments (84% OTD) drove the most delays. Air Charter, conversely, performed perfectly.
- **Lead Time Insights:** Highlighted massive variability between Air (**88 days**) and Ocean (**144 days**), necessitating distinct operational planning horizons.

## **Recommendations (Operational Scripts)**

- **Spend Negotiation Roadmap:** Direct all immediate vendor cost-reduction negotiations toward the ARV and HRDT product groups, as they control the overwhelming majority of the budget.
- **Routing Strategy Lever:** Execute a cost-benefit analysis on shifting critical, low-volume shipments to Air Charter to immediately improve network reliability.
- **Inventory Calibration:** Update inventory reorder points across all hubs to reflect the newly calculated, real-world lead times by mode.

## **Next Steps**

- **Golden Pipeline Maintenance:** Automate the Python data pipeline using `supply_chain.ipynb` to ingest raw CSVs and generate clean outputs (`shipping_data_clean.csv`) on a strict schedule.
- **Proactive Alerting:** Establish threshold alerts within the dashboard to trigger warnings the moment a specific vendor's OTD rate drops below the 88% operational standard.
