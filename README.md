# Hi, I'm Paul 👋
### Analytics Engineer | SQL, Python, Power Query (M) & Power BI Architect

I build **resilient data pipelines** that bridge the gap between raw database architecture and executive-level insights. I specialize in backend data transformations using **Python and optimized SQL**, advanced Power Query (M) engineering, and **sophisticated Power BI modeling** to transform complex, messy environments into high-performance, interactive dashboards that drive decisions.

---

## 🚀 Featured Project 1: Enterprise Subscription Revenue Audit & Integrity Pipeline
**Stack:** Python (Pandas) + PostgreSQL + Power BI + DAX

This project solves the "Ghost Revenue" and financial reporting inflation problem caused by upstream CRM/Billing system synchronization failures.

- **The Problem:** Upstream database glitches failed to flip the `auto_renew` flag to false upon customer cancellation (`churn_flag = True`), leading standard financial reports to blindly over-calculate and misreport active Monthly Recurring Revenue (MRR).
- **The Solution:** Engineered a decoupled dual-view database architecture in PostgreSQL to separate operational metrics from system auditing, utilizing a Python preprocessing layer to programmatically clean and normalize raw files before database ingestion.
- **Technical Impact:** - **Python Ingestion & Cleansing (Pandas):** Programmatically extracted and processed raw subscription and account datasets; engineered automated data-cleaning rules to drop invalid records with negative revenue anomalies.
  - **Defensive Data Formatting:** Utilized Pandas to apply an engineering placeholder (`2099-12-31`) to missing attrition dates, standardizing the schema and optimizing downstream SQL date-math calculations.
  - **Audit View Architecture:** Developed a specialized PostgreSQL view (`v_revenue_inflation_audit`) leveraging targeted conditional logic to isolate discrepancies and calculate cumulative historical "paper leakage" for executive-level review.
  - **Production View Engine:** Formulated a clean, true revenue reporting view (`v_true_revenue_reporting`) to enforce bulletproof business logic at the source, forcing churned accounts to zero and keeping downstream BI calculations lean and fast.
  - **Source-Side Optimization:** Shifted heavy analytical workloads from the presentation layer (Power BI) into the database layer, keeping DAX measures basic and optimizing dashboard load times.

[View Project Details](https://github.com/pjtheprogrammer/Enterprise-Subscription-Revenue-Audit-Integrity-Pipeline)

---

## 🚀 Featured Project 2: End-to-End SaaS Revenue Engine
**Stack:** PostgreSQL + Power BI + DAX

This project solves the "Hidden Churn" problem by architecting a three-state subscription model.

- **The Problem:** Standard reporting failed to account for "Pending" revenue and "Future-Dated" churn, leading to inaccurate MRR projections.
- **The Solution:** - Engineered a **PostgreSQL View** to handle temporal status logic at the source.
  - Developed a **Defensive DAX Layer** to protect against "Divide by Zero" errors.
  - Created an interactive dashboard for real-time MRR and Churn tracking.
- **Technical Impact:** - **Source-Side Logic:** Moved complex subscription state classification (Active/Pending/Churned) into a SQL View to ensure a "Single Source of Truth" and reduce BI-layer overhead.
  - **Defensive DAX Architecture:** Implemented fail-safe measures using the `DIVIDE` function and strict data-type enforcement to prevent NaN/Infinity errors during period-over-period calculations.

[View Project Details](https://github.com/pjtheprogrammer/End-to-End-Saas-Revenue-Engine)

---

## 🚀 Featured Project 3: Supply Chain Routing Efficiency & Anomaly Detection Pipeline
**Stack:** Python (Pandas/NumPy/Geopy) + PostgreSQL + Power BI

This project delivers an end-to-end data pipeline designed to programmatically surface operational waste and routing anomalies across 50,000 global delivery orders.

- **The Problem:** Logistics platforms lack visibility into physical routing overhead, masking hidden inefficiencies when actual dispatch routes wildly exceed baseline distance calculations. 
- **The Solution:** Engineered an automated geospatial and data cleansing pipeline that quantifies routing delta errors, captures faulty or corrupted order records at the database level, and projects a live regional risk map for supply chain managers.
- **Technical Impact:**
  - **Geospatial Feature Engineering:** Utilized Python to parse coordinate data and calculate precise straight-line geodetic profiles; engineered an automated **Distance Delta** metric ($Route\ Distance - Straight\ Line\ Distance$) to dynamically score hub efficiency.
  - **Defensive Data Cleaning:** Created an automated database filtration layer to isolate upstream system anomalies—such as unassigned orders (null `hub_id` values) and broken numeric ranges (negative weights or distance values)—preserving downstream reporting integrity.
  - **High-Density Mapping Interface:** Designed a live-connected Power BI geospatial layout utilizing conditional gradient structures anchored directly to the calculated Distance Delta metrics to instantly surface underperforming warehouses.

[View Project Details](https://github.com/pjtheprogrammer/Enterprise-Supply-Chain-Routing-Efficiency-Anomaly-Detection-Pipeline)

---

## 🛠️ Tech Stack
- **Data Engineering:** Python, Advanced Power Query (M), PostgreSQL, SQL Server
- **BI & Visualization:** Power BI (Desktop & Service), Excel (Power Pivot)
- **Architecture:** ETL/ELT Pipelines, Data Integrity Auditing, Query Folding Optimization, Relational Modeling
- **Version Control:** Git, GitHub

---

## 📬 Connect with me:
- **Email:** paulefeoku@hotmail.com
