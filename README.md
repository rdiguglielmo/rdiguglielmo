# 📊 Data Portfolio

I build data pipelines end to end — from raw public-sector and regulatory sources to dimensional
models and Power BI reports, across local, lakehouse and cloud warehouse environments.

[LinkedIn](https://www.linkedin.com/in/rdiguglielmo) ·
[Upwork](https://www.upwork.com/freelancers/~01bf95ce2c78bcf992)

## 📚 Table of Contents

- [Data Engineering](#data-engineering)
- [Data Analytics](#data-analytics)
- [Business Intelligence](#business-intelligence)
- [In Progress](#in-progress)
- [Tech Stack](#tech-stack)

## Data Engineering

| Project | Tools | Description |
|---|---|---|
| 📊 [SEC EDGAR Financial Statements Pipeline](https://github.com/rdiguglielmo/sec-edgar-financial-pipeline) | Python, DuckDB, dbt, SQL, Power BI | End-to-end pipeline that turns 18 million rows of raw SEC XBRL filings into a tested star schema for financial analysis. Every double-counting hazard in the source is an explicit, tested, documented flag, and every figure on the dashboard is checked against a written expectation before it ships. Runs on a laptop: no cloud account, no credentials. |

## Data Analytics

| Project | Tools | Description |
|---|---|---|
| 📈 [US Restaurant Sector — Financial Analysis](https://github.com/rdiguglielmo/us-restaurant-financials-analysis) | SQL, DuckDB, Python, Power BI | Takes an evidence-based position on the relative financial health of ten listed restaurant companies: Yum China and Chipotle lead, and Bloomin' and Papa John's trail, whichever ranking pillar is left out. It is built on the warehouse above and reproduces that project's published figures before trusting a ratio of its own. Every figure names the query or filing behind it. |

## Business Intelligence

| Project | Tools | Description |
|---|---|---|
| 🎨 [Power BI Theme Lab](https://github.com/rdiguglielmo/powerbi-theme-lab) | Node.js, Power BI, WCAG | A complete Power BI theme compiled from a short list of design tokens, with every colour pair it produces audited against the WCAG contrast formula. The [live gallery](https://rdiguglielmo.github.io/powerbi-theme-lab/) shows the same report in six themes, where every figure is identical and only the palette moves. |

## In Progress

Described before they are built, because writing down what a project has to demonstrate is what
keeps its scope honest. Listed without links until the repository exists.

| Project | Tools | Description |
|---|---|---|
| 🚢 EU Trade Lakehouse | Databricks, PySpark, Delta, Power BI | Processes detailed EU import and export data through bronze, silver and gold layers. |
| 🏛 EU Public Procurement Pipeline | Airflow, GCS, BigQuery, dbt, Python, XML, Power BI | Orchestrated cloud pipeline over EU tender notices for public spend analytics. |

## Tech Stack

Only what is actually demonstrated in a repository above. This section grows as the projects do.

| Category | Tools |
|---|---|
| Languages | Python, SQL, Node.js |
| Transformation | dbt |
| Storage and formats | DuckDB, Parquet |
| BI and reporting | Power BI, DAX, Power Query |
| Practices | Dimensional Modeling, Data Quality, Incremental Ingestion, Financial Statement Analysis, Design Systems, Accessibility (WCAG) |
| Tooling | Git |
