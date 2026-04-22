# Hi, I'm Paul 👋
### Analytics Engineer | SQL, Power Query(M) & Power BI Architect

I build **resilient data pipelines** that bridge the gap between raw database architecture and executive-level insights. I specialize in **Advanced Power Query (M) engineering**, SQL optimization, and **sophisticated Power BI modeling** to transform complex environments into high-performance, interactive dashboards that drive decisions.

---

## 🚀 Featured Project: End-to-End SaaS Revenue Engine
**Stack:** PostgreSQL + Power BI + DAX

This project solves the "Hidden Churn" problem by architecting a three-state subscription model.

- **The Problem:** Standard reporting failed to account for "Pending" revenue and "Future-Dated" churn, leading to inaccurate MRR projections.
- **The Solution:** - Engineered a **PostgreSQL View** to handle temporal status logic at the source.
  - Developed a **Defensive DAX Layer** to protect against "Divide by Zero" errors.
  - Created an interactive dashboard for real-time MRR and Churn tracking.
- **Technical Impact:** - **Source-Side Logic:** Moved complex subscription state classification (Active/Pending/Churned) into a SQL View to ensure a "Single Source of Truth" and reduce BI-layer overhead.
  - **Defensive DAX Architecture:** Implemented fail-safe measures using the `DIVIDE` function and strict data-type enforcement to prevent NaN/Infinity errors during period-over-period calculations.

[View SQL & DAX Code](./SaaS-Postgres-Folder) | [See Dashboard Screenshot](./SaaS-Postgres-Folder/dashboard.png)

---

## 📊 Case Study 1: Global Sales & Profit Intelligence Suite
**Stack:** Power Query (Advanced ETL) + Power BI + DAX

- **The Problem:** Manual reconciliation of 10,000+ global transactions caused massive reporting bottlenecks and delayed visibility into net profit margins.
- **The Solution:** Engineered a centralized data engine that automates the consolidation of disparate regional datasets into a single "Source of Truth."
- **Technical Impact:** Built a self-maintaining **Power Query** pipeline for instant data transformation and developed dynamic **DAX** monitoring for real-time Net Profit vs. Gross Sales tracking.

[View Project Details](./Global-Sales-Folder)

---

## 🎯 Case Study 2: CRM Sales Funnel & Conversion Dashboard
**Stack:** Power BI + Power Query + Advanced Data Modeling

- **The Problem:** Sales tracking was plagued by "data inflation" and manual errors, making it impossible to identify where deals were "leaking" from the funnel.
- **The Solution:** Designed a "Dual-State" tracking system and a cohort-based logic engine to monitor deal transitions from Proposal to Closed.
- **Technical Impact:** - **Automated Conversion Engine:** Engineered cross-table logic to eliminate "double-counted" leads and ensure pipeline accuracy.
  - **Operational Leakage Analysis:** Built visual diagnostic tools to pinpoint exact drop-out stages, enabling targeted process improvements.

[View Project Details](./CRM-Sales-Folder)

---

## 🔄 Case Study 3: SaaS Revenue & Churn Intelligence
**Stack:** Power BI + Power Query + Time Intelligence (DAX)

- **The Problem:** Subscription data was trapped in disorganized spreadsheets with inconsistent types and no way to calculate dynamic Active MRR.
- **The Solution:** Implemented a full-stack BI solution featuring a Star Schema model and a dedicated Calendar table for advanced Time Intelligence.
- **Technical Impact:** - **ETL & Engineering:** Used Power Query to enforce strict schemas and resolve date-type discrepancies.
  - **Advanced DAX:** Authored complex measures using `CALCULATE` and `FILTER` to handle date-range logic for Running Totals.

[View Project Details](./SaaS-Intelligence-Folder)

---

## 🛠️ Tech Stack
- **Data Engineering:** Advanced Power Query (M), PostgreSQL, SQL Server
- **BI & Visualization:** Power BI (Desktop & Service), Excel (Power Pivot)
- **Architecture:** ETL/ELT Pipelines, Query Folding Optimization, Relational Modeling
- **Version Control:** Git, GitHub

---

## 📬 Connect with me:
- **Email:** paulefeoku@hotmail.com
