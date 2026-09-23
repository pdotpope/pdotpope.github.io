---
icon: material/movie-open
tags:
  - Python
  - Snowflake
  - dbt
  - ETL
  - Streamlit
  - Data Modeling
---

# PMDb

> *Interactive web app showcasing a Snowflake database of 37,000+ films with IMDb and Letterboxd ratings*

[:material-web: Live Site](https://pmoviedb.streamlit.app){ .md-button .md-button--primary target="_blank" rel="noopener" }

![App Preview](../assets/pmdb-ss.jpg)

## Overview

- An end-to-end medallion pipeline: raw Kaggle datasets land in Snowflake as bronze tables, dbt models clean and join them into silver and gold layers, and a Streamlit app presents the results
- **Explore film rankings across multiple rating systems** with leaderboards filtering by decade, popularity, and rating
- **Compare IMDb vs Letterboxd lean** using rating differentials to highlight where the platforms disagree most

## Tech Stack

| Layer | Tools | Description |
|---|---|---|
| **Ingestion** | Python, Snowflake Connector | Loads raw Kaggle datasets into Snowflake as *bronze* tables |
| **Modeling** | dbt Core | Standardizes types and filters nulls into *silver* tables, then joins both platforms on title + year to compute composite ratings and differentials in a *gold* table |
| **Presentation** | Streamlit, Plotly | Renders interactive charts and film lookup from a periodic static export of the gold table |

## Skills Developed

- Medallion (bronze/silver/gold) architecture
- Transformation modeling with dbt
- Cloud data warehousing in Snowflake

---

[:fontawesome-brands-github: Source Code](https://github.com/pdotpope/pmdb){ .md-button .md-button--primary target="_blank" rel="noopener" }
