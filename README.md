# 🏏 FantasyEdge  
### An End-to-End Fantasy Sports Data Engineering & Analytics Platform

FantasyEdge is an end-to-end fantasy sports analytics platform designed to demonstrate **production-style data engineering**, analytics modeling, and data consumption through modern interfaces.  
The project focuses on ingesting real-world sports data, transforming it into analytics-ready structures, and serving curated insights for fantasy sports decision-making.

---

## 🎯 Project Objective

To build a scalable data engineering pipeline that:
- Ingests historical sports data
- Applies structured transformations and feature engineering
- Computes fantasy-specific performance metrics
- Exposes analytics via APIs and dashboards
- Powers a mobile-first fantasy insights experience

This project mirrors the architecture and workflows used by real-world fantasy sports platforms.

---

## 📊 Initial Scope

- **Sport:** Cricket  
- **League:** Indian Premier League (IPL)  
- **Data Type:** Historical match & player performance data  
- **Focus:** Batch processing & analytics (live data optional later)

---

## 🧱 High-Level Architecture

```
Sports Data Sources (CSV / API)
        ↓
Raw Data Lake (Parquet)
        ↓
Processing Layer (Pandas / PySpark)
        ↓
Analytics Storage (PostgreSQL / Parquet)
        ↓
FastAPI (Read-only Analytics APIs)
        ↓
Mobile App / BI Dashboards
```

---

## 🗂️ Data Sources (Phase 1)

Publicly available IPL datasets containing:
- Match metadata
- Player details
- Ball-by-ball performance data

Primary source:
- Kaggle IPL historical datasets

All data is treated as **immutable raw input** and stored in Parquet format.

---

## 🗃️ Data Modeling Approach

The analytics layer follows a **star schema** optimized for reporting and fantasy analysis.

### Fact Tables
- Player match performance
- Fantasy points per match
- Team match results

### Dimension Tables
- Players
- Teams
- Matches
- Seasons
- Venues

---

## ⚙️ Tech Stack

**Language**
- Python

**Data Processing**
- Pandas
- PySpark

**Storage**
- Parquet (data lake)
- PostgreSQL (analytics layer)

**Backend**
- FastAPI (read-only analytics APIs)

**Visualization & BI**
- Power BI
- Plotly / Matplotlib

**Web / Mobile**
- Streamlit (initial validation)
- Flutter (mobile app – planned)

**Orchestration**
- Apache Airflow / Cron

**Optional Enhancements**
- Kafka (streaming)
- AWS Glue & Athena

---

## 📁 Repository Structure (Planned)

```
fantasyedge/
│
├── ingestion/          # Data ingestion scripts
├── transformations/    # Cleaning & feature engineering
├── fantasy_engine/     # Fantasy scoring logic
├── analytics/          # Aggregations & metrics
├── api/                # FastAPI backend
├── mobile_app/         # Flutter app (planned)
├── dashboards/         # Power BI assets
├── data/
│   ├── raw/
│   ├── processed/
│   └── curated/
├── docs/
│   └── data_sources.md
└── README.md
```

---

## 🚧 Project Status

- [x] Project scoping & architecture
- [x] Data source selection
- [ ] Raw data ingestion
- [ ] Data transformations
- [ ] Fantasy scoring engine
- [ ] FastAPI analytics layer
- [ ] Dashboards & mobile app

---

## 💡 Key Learning Outcomes

- End-to-end data engineering pipeline design
- Analytics-ready data modeling
- Fantasy sports domain logic
- API-first data consumption
- BI & mobile integration

---

## 🔮 Future Enhancements

- Live match streaming via Kafka
- Machine learning-based player projections
- Feature store for reusable metrics
- Cloud-native deployment

---

## 📌 Why FantasyEdge?

FantasyEdge is built to **showcase how data engineering enables products**, not just pipelines — combining data ingestion, modeling, analytics, and real user-facing consumption.
