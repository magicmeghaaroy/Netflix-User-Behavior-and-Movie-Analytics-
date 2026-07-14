# 📊 Netflix User Behavior & Movie Analytics

[👉 Click Here to View My Visual Case Study Portfolio on Maven Analytics](https://mavenshowcase.com/project/57099)

<img width="1442" height="844" alt="CEO Dashboard" src="https://github.com/user-attachments/assets/cb2f9b5a-d58e-4385-b278-2c96d70b98c1" />

## 📌 Project Overview - CEO Dashboard

An executive-level Power BI business intelligence solution built in Sleek Dark Mode. This dashboard transforms raw, multi-table platform logs into actionable analytics regarding subscriber engagement, content catalog expansion, and streaming performance metrics.

## 🛠️ Tech Stack & Advanced Data Skills
* **BI Tool:** Power BI Desktop
* **Data Modeling:** Advanced Star Schema Design (1-to-Many Single Direction `1 --> *`)
* **Data Engineering (ETL):** Power Query text manipulation, column splitting, and type enforcement.
* **DAX Engineering:** Custom Time Intelligence matrices, advanced filtering, and dynamic KPI tracking.

## 🏗️ Data Architecture (Star Schema)
This project rejects flat-file frameworks in favor of a performant, production-ready corporate schema layout. 
* **Fact Tables (Transaction Logs):** `watch_history`, `recommendation_logs`, `search_logs`, `reviews`
* **Dimension Tables (Lookup Arrays):** `users`, `movies`, and a custom-built, sorted `Dim_Date` calendar framework.

## 🧮 Core DAX Measures Modeled

### 1. Platform Scale (Total Active Viewers)
Tracks distinct audience footfall over customizable chronological snapshots.
```dax
Total Viewers = DISTINCTCOUNT(watch_history[user_id])
```

### 2. Deep Engagement Metric (Total Operational Stream Hours)
Converts raw application process logs from baseline streaming minutes into clean business metrics.
```dax
Total Watch Time (Hrs) = SUM(watch_history[watch_duration_minutes]) / 60
```

### 3. Content Performance Standard (Average Retention Rate)
Adjusts raw percentage logs to conform with Power BI decimal modeling standards.
```dax
Avg Completion Rate = DIVIDE(AVERAGE(watch_history[progress_percentage]), 100, 0)
```

## 📈 Strategic Business Insights Identified
* **Catalog Engagement:** Content completion analytics directly dictate platform retention—low completion segments isolate specific genres requiring library maintenance.
* **Interactive Navigation:** Designed an integrated dark mode slicer layout panel optimizing user query drilling down across specific genres and core language matrices seamlessly.

---
*Developed by magicmeghaaroy as part of a professional BI engineering portfolio project.*
