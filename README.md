<div align="center">

### I build data pipelines end to end

From raw public-sector and regulatory sources to dimensional models and Power BI dashboards,
across local, lakehouse and cloud warehouse environments.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rdiguglielmo)
[![Upwork](https://img.shields.io/badge/Upwork-6FDA44?style=for-the-badge&logo=upwork&logoColor=white)](https://www.upwork.com/freelancers/~01bf95ce2c78bcf992)

</div>

---

## About

I work on the whole path a number travels: pulling it out of a public source that was never designed
for analysis, modelling it so it can be aggregated without lying, checking it, and putting it in
front of someone who has to decide something.

The part I care most about is the failure that does not announce itself. A scope rule that quietly
dropped McDonald's out of its own industry. Report cards at 1.10:1 contrast — edges that cost
something and separated nothing. A card sized a little too small that shipped `40 filinqs` across
three pages, because a clipped descender reads as a font quirk. None of those crashed anything, and
none were caught by re-reading the code. Everything below is built so that class of error has
somewhere to show up.

---

## Featured work

### SEC EDGAR Financial Statements Pipeline

**[rdiguglielmo/sec-edgar-financial-pipeline](https://github.com/rdiguglielmo/sec-edgar-financial-pipeline)**

18 million rows of raw SEC XBRL filings turned into a tested star schema for financial analysis.
Every double-counting hazard in the source is an explicit, tested, documented flag, and every figure
on the dashboard is checked against a written expectation before it ships. Runs on a laptop: no
cloud account, no credentials.

[![Executive Overview dashboard](https://raw.githubusercontent.com/rdiguglielmo/sec-edgar-financial-pipeline/main/powerbi/screenshots/01-executive-overview.png)](https://github.com/rdiguglielmo/sec-edgar-financial-pipeline#step-7-dashboard)

| | |
|---|---|
| **Raw rows ingested** | 17,962,229 across four stacked tables |
| **Transformation** | 11 dbt models: 5 staging, 5 dimensions, 1 fact |
| **Data quality** | 156 checks — 146 pass, and **10 fail on purpose**, each declaring its expected failure count |
| **Dashboard** | 3 Power BI pages, one of them reporting on the pipeline's own inputs |

What the data turned out to say:

- **Net margin inside a single industry runs from 32.2% to below zero.** In the same quarter,
  McDonald's turned 7,078 m USD of revenue into a 32.2% net margin while Bloomin' Brands lost 4.9%
  on 929 m. Both are restaurant companies.
- **96.24% of the accounting vocabulary carries 8.54% of the numbers.** 317,473 of 329,861 concepts
  are company-invented. `NonCashLeaseExpense` and `NoncashLeaseExpense` are the same concept split
  across two strings that nothing in the source relates to each other.
- **One fact in seven is reported more than once, and 1.37% of those change.** Counting restatements
  names the wrong companies; the share identifies them — Azenta restated 252 of 402 facts, 62.7%.

**[Read the full write-up](https://github.com/rdiguglielmo/sec-edgar-financial-pipeline)** —
architecture, star schema, the ten modelling decisions with what was discarded, and the queries
behind every number above.

<br>

### Power BI Theme Lab

**[rdiguglielmo/powerbi-theme-lab](https://github.com/rdiguglielmo/powerbi-theme-lab)**

A complete Power BI theme compiled from a short list of design tokens, with every colour pair it
produces audited against the WCAG contrast formula. Change the tokens and the same report arrives in
a different set of clothes without a single page being edited.

<table>
<tr>
<td width="50%"><a href="https://rdiguglielmo.github.io/powerbi-theme-lab/"><img src="https://raw.githubusercontent.com/rdiguglielmo/powerbi-theme-lab/main/docs/shots/cypress-01.jpg" alt="The Executive Overview page rendered in the Cypress theme"></a></td>
<td width="50%"><a href="https://rdiguglielmo.github.io/powerbi-theme-lab/"><img src="https://raw.githubusercontent.com/rdiguglielmo/powerbi-theme-lab/main/docs/shots/perf-dark-01.jpg" alt="The Executive Overview page rendered in the Performance Dark theme"></a></td>
</tr>
<tr>
<td><em>Cypress.</em></td>
<td><em>Performance Dark.</em></td>
</tr>
</table>

That is the page at the top of this README, in two of the six themes. Not a single visual was
positioned or coloured by hand — the pages, the harness and the theme are all written by scripts,
which is the whole reason a theme swap can be trusted to change nothing but the palette.

**[Open the gallery](https://rdiguglielmo.github.io/powerbi-theme-lab/)** — 18 renders, three report
pages across six themes, each with its measured contrast ratio.

---

## Tech Stack

Only what is actually demonstrated in a repository above. This section grows as the projects do.

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-025E8C?style=flat-square)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white)

**Transformation and storage**

![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white)
![DuckDB](https://img.shields.io/badge/DuckDB-FFF000?style=flat-square&logo=duckdb&logoColor=black)
![Parquet](https://img.shields.io/badge/Parquet-50ABF1?style=flat-square&logo=apacheparquet&logoColor=white)

**BI and reporting**

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-F2C811?style=flat-square)
![Power Query](https://img.shields.io/badge/Power%20Query-F2C811?style=flat-square)

**Practices**

![Dimensional Modeling](https://img.shields.io/badge/Dimensional%20Modeling-475569?style=flat-square)
![Data Quality](https://img.shields.io/badge/Data%20Quality-475569?style=flat-square)
![Incremental Ingestion](https://img.shields.io/badge/Incremental%20Ingestion-475569?style=flat-square)
![Design Systems](https://img.shields.io/badge/Design%20Systems-475569?style=flat-square)
![Accessibility](https://img.shields.io/badge/Accessibility%20%28WCAG%29-475569?style=flat-square)

**Tooling**

![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

---

<details>
<summary><b>What is next</b> — three projects in progress</summary>

<br>

Described before they are built, because writing down what a project has to demonstrate is what
keeps its scope honest. Listed without links until the repository exists.

| Project | Stack & Skills | What it will do |
|---|---|---|
| US Public Companies — Financial Analysis | SQL, Python, Power BI, Financial Analysis, Storytelling | Takes an evidence-based position on the performance of listed companies, on top of the warehouse above |
| EU Trade Lakehouse | Databricks, PySpark, Delta, Medallion Architecture, Power BI | Processes detailed EU import and export data through bronze, silver and gold layers |
| EU Public Procurement Pipeline | Airflow, GCS, BigQuery, dbt, Python, XML, Power BI | Orchestrated cloud pipeline over EU tender notices for public spend analytics |

</details>
