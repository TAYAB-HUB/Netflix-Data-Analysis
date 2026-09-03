# 🏠 Airbnb Market & Listing Performance Dashboard

[![Power BI](https://img.shields.io/badge/Power_BI-Desktop-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Calculations-0078D4?style=for-the-badge)](https://learn.microsoft.com/en-us/dax/)
[![Power Query](https://img.shields.io/badge/Power_Query-ETL-2C82C9?style=for-the-badge)](https://powerquery.microsoft.com/)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/TAYAB-HUB/Airbnb-Performance-Dashboard)

An interactive, enterprise-grade **Power BI Business Intelligence Dashboard** analyzing Airbnb's listing growth, market concentration, room pricing tiers, city-level rating matrices, and customer review seasonality across major global markets.

---

## 📑 Table of Contents
- [Executive Summary & Purpose](#-executive-summary--purpose)
- [Tech Stack & Architecture](#-tech-stack--architecture)
- [Data Source & Scale](#-data-source--scale)
- [Key KPIs & Metrics](#-key-kpis--metrics)
- [Dashboard Walkthrough & Insights](#-dashboard-walkthrough--insights)
- [DAX Measures Showcase](#-dax-measures-showcase)
- [Business Impact & Strategic Takeaways](#-business-impact--strategic-takeaways)
- [Screenshots & Demo](#-screenshots--demo)
- [Author & Contact](#-author--contact)

---

## 🔍 Executive Summary & Purpose

Operating in hyper-competitive short-term rental markets requires dynamic visibility into supply growth, customer sentiment, and pricing power. This project consolidates **279,000+ listings** across **10 international cities** to help property managers, commercial strategists, and marketing teams make data-backed expansion and pricing decisions.

---

## 🛠 Tech Stack & Architecture

- **Business Intelligence Platform:** Power BI Desktop
- **ETL & Data Transformation:** Power Query (M Language)
- **Calculations & Business Logic:** DAX (Data Analysis Expressions)
- **Data Modeling:** Star / Relational Schema linking Listings, Hosts, Cities, Room Types, and Reviews
- **Deliverables:** `.pbix` (Interactive Dashboard), `.pdf` / `.png` (Executive Presentation)

---

## 📊 Data Source & Scale

| Metric | Volume / Scope |
| :--- | :--- |
| **Total Listings Analyzed** | **279,712** listings |
| **Total Hosts** | **182,024** hosts |
| **Total Reviews Processed** | **187,999** customer reviews |
| **Global Markets** | **10** major international cities |
| **Property Types** | **144** unique accommodation categories |

---

## 🎯 Dashboard Walkthrough & Insights

### 1. 📈 Historical Listing Growth Trend (2008–2021)
- **Pattern:** Rapid expansion peaking in **2015**, followed by market consolidation in 2016–2017, steady recovery in 2018–2019, and a sharp contraction during 2020 due to global travel restrictions.

### 2. 🌍 Market Share by City & Superhost Distribution
- **Concentration:** **Paris, New York, and Sydney** account for nearly **50% of platform listings** and **48% of total customer reviews**.
- **Superhost Advantage:** Cities with higher Superhost ratios exhibit higher median ratings across cleanliness and communication.

### 3. 💵 Average Price by Room Type
- **Hotel Rooms:** **$800 / night** (Premium commercial tier)
- **Entire Places:** **$673 / night** (High-demand family & group tier)
- **Shared Rooms:** **$580 / night**
- **Private Rooms:** **$462 / night** (High-volume budget tier)

### 4. ⭐ City Ratings Matrix
- Benchmarks customer satisfaction across 5 core dimensions: *Accuracy, Communication, Cleanliness, Location, and Value*.
- **Top Performer:** **Mexico City** consistently achieved high scores across cleanliness and value-for-money metrics.

### 5. 🔍 Review Behavior & Anomaly Detection
- **Distribution:** **98.8% of customers** submitted $\le 3$ reviews.
- **Anomaly:** Identified an extreme outlier profile with **283 reviews**, highlighting an opportunity for automated scraping-bot detection and data auditing.

### 6. 📅 Monthly Review Distribution (Travel Seasonality)
- **European Summer Peak:** **Paris and Rome** dominate activity between **April and August**.
- **Holiday Winter Surge:** **New York** sees significant volume surges during **November and December**.

---

## 🧮 DAX Measures Showcase

Sample DAX calculations implemented in this model:

```dax
// 1. Total Active Listings
Total Listings = COUNTROWS('Listings')

// 2. Superhost Ratio
Superhost % = 
DIVIDE(
    CALCULATE(COUNTROWS('Listings'), 'Listings'[host_is_superhost] = "t"),
    COUNTROWS('Listings'),
    0
)

// 3. Average Price by Filtered Context
Average Accommodation Price = AVERAGE('Listings'[price])

// 4. City Market Share
City Market Share % = 
DIVIDE(
    COUNTROWS('Listings'),
    CALCULATE(COUNTROWS('Listings'), ALLSELECTED('Listings'[city])),
    0
)
```


---

## 💡 Business Impact & Strategic Takeaways

1. **Regional Marketing Alignment:** Allocate digital ad budgets to European destinations (Paris, Rome) during Q2/Q3, and redirect holiday campaigns to New York in Q4.
2. **Dynamic Pricing Benchmarking:** Position entire apartments and boutique hotel listings to capture high willingness-to-pay segments ($650–$800+ range).
3. **Superhost Incentivization:** Expand host training and Superhost badge rewards in emerging markets to directly uplift low cleanliness and communication scores.
4. **Data Integrity Auditing:** Implement automated validation rules to flag anomalous high-frequency review accounts before feed aggregation.

---

## 🖼 Screenshots & Demo

<p align="center">
  <img src="Overview.png" width="95%" alt="Airbnb Dashboard Overview" />
</p>

<p align="center">
  <img src="Market share and Ratings .png" width="95%" alt="Airbnb Market Share and Ratings" />
</p>

<p align="center">
  <img src="Review Frequency and Seasonality.png" width="95%" alt="Airbnb Review Frequency and Seasonality" />
</p>

---

## 👤 Author & Contact

**Syed Mohammed Tayab**  
- **Email:** [syedtayab01@gmail.com](mailto:syedtayab01@gmail.com)  
- **LinkedIn:** [linkedin.com/in/syed-tayab01](https://www.linkedin.com/in/syed-tayab01)  
- **GitHub:** [github.com/TAYAB-HUB](https://github.com/TAYAB-HUB)  
