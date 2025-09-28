# Netflix Content Strategy — Catalog Analytics (Python · VS Code · Jupyter)

> This repository turns the public Netflix catalog metadata into clear, business-ready insights a content team can act on.  
> Focus: **data/business analytics** (no ML). I run everything from a single Jupyter notebook in VS Code.

---

## 📌 Why I built this

Streaming teams constantly ask:
- *What should we commission next and in which market?*
- *Is our catalog balanced across ratings and genres?*
- *Where are we under-serving viewers by genre and country?*

This project answers those questions with a transparent, reproducible analysis of the Netflix catalog dataset from **Kaggle** (`netflix_titles.csv`). It avoids machine learning and stays squarely within an analyst’s toolkit: data cleaning, feature engineering, descriptive analytics, and crisp visuals.

---

## 🧠 Business problems & how this notebook solves them

1) **Catalog Evolution (Supply Mix)**
   - **Question:** How has the catalog grown by *type* (Movies vs TV Shows) over time?
   - **What I do:** Compute and plot titles added per year by type.
   - **Why it matters:** Guides portfolio planning (e.g., rebalance movie/show mix).

2) **Ratings Composition (Maturity Profile)**
   - **Question:** What is the distribution of content ratings (e.g., TV-14, PG-13)?
   - **What I do:** Produce a rating distribution table + chart.
   - **Why it matters:** Signals if family or adult segments need refresh.

3) **Genre Concentration (What We’re Known For)**
   - **Question:** Which genres dominate the catalog overall and by type?
   - **What I do:** Build a **Top Genres** table and a **Genre × Type** heatmap.
   - **Why it matters:** Identifies crowded vs. niche areas to inform slate balance.

4) **Country–Genre Content Gaps (Where to Invest)**
   - **Question:** Which genres are **under-indexed** within a given country relative to global share?
   - **What I do:** Compute  
     `gap = country_share(genre) – global_share(genre)`  
     and visualize the most under-represented genres for a selected country (e.g., France/India/US).
   - **Why it matters:** Directly suggests **acquisition/commission** opportunities by market.

5) **Viewing Time (Operational Lens)**
   - **Question:** Which genres tend to run longer/shorter?
   - **What I do:** Parse duration and chart **median movie duration by genre**.
   - **Why it matters:** Helps programming calendars and “time to watch” UX rows.

> **Scope note:** I intentionally removed “time-to-platform” and “cleaned CSV export” steps to keep the analysis focused for recruiters and content stakeholders.

---

## 🗂️ Repository structure

