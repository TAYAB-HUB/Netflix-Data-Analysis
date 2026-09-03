# 🎬 Netflix Original Films & IMDB Scores: Exploratory Data Analysis

[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-1.3+-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualizations-4C72B0?style=for-the-badge)](https://seaborn.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Plotting-11557C?style=for-the-badge)](https://matplotlib.org/)
[![Plotly](https://img.shields.io/badge/Plotly-Interactive-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)](https://plotly.com/)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/TAYAB-HUB/Netflix-Data-Analysis)

An in-depth **Exploratory Data Analysis (EDA)** on Netflix Original films to uncover what drivers influence critical success, viewer reception, and **IMDB ratings**. This project bridges data manipulation, statistical visualization, and strategic streaming business intelligence.

---

## 📑 Table of Contents
- [Overview](#-overview)
- [Dataset Architecture](#-dataset-architecture)
- [Tech Stack & Tools](#-tech-stack--tools)
- [Research Questions & Key Findings](#-research-questions--key-findings)
- [How to Run This Project](#-how-to-run-this-project)
- [Strategic Business Recommendations](#-strategic-business-recommendations)
- [Author & Contact](#-author--contact)

---

## 🔍 Overview

With global streaming platforms investing billions in original content, understanding subscriber preferences and critical acclaim is vital. This project conducts end-to-end data cleaning, anomaly detection, categorical aggregation, and correlation analysis on Netflix Original releases up to June 1st, 2021.

Key goals:
- Identify runtime, genre, and language drivers that correlate with higher IMDB scores.
- Uncover seasonal and yearly release trends.
- Deliver data-backed content strategy recommendations for streaming production teams.

---

## 📊 Dataset Architecture

The dataset includes all Netflix Original films released up to **June 1, 2021**, integrated with corresponding IMDB ratings and metadata:

- **Source:** Web-scraped Wikipedia Netflix Originals integrated with Kaggle IMDB dataset.
- **Key Attributes:**
  - `Title`: Film name
  - `Genre`: Primary content category (50+ categories)
  - `Premiere`: Official global release date
  - `Runtime`: Duration in minutes
  - `IMDB Score`: User rating metric (0.0 to 10.0)
  - `Language`: Primary spoken audio language

---

## 🛠 Tech Stack & Tools

- **Language:** Python 3.x
- **Data Manipulation:** `pandas`, `numpy`
- **Static Visualization:** `seaborn`, `matplotlib`
- **Interactive Visualization:** `plotly`
- **Environment:** Jupyter Notebook, VS Code

---

## 📈 Research Questions & Key Findings

### 1. In which languages were the longest-running films created?
- **Finding:** English and Hindi films exhibited the widest runtime distributions, with specialized international epics recording runtimes exceeding 140+ minutes.
<p align="center">
  <img src="https://github.com/user-attachments/assets/3d44f6cd-dd13-4a54-8e98-ec46424a6333" width="90%" alt="Box plot graph for Runtime by Language" />
</p>

---

### 2. What are the IMDB ratings of Documentaries shot between Jan 2019 and June 2020?
- **Finding:** Documentaries consistently maintain higher median IMDB scores (~7.0 - 8.5) compared to general fiction releases, demonstrating strong niche viewer retention.
<p align="center">
  <img src="https://github.com/user-attachments/assets/fb1f8b4d-2f6d-417c-a592-86967e897e43" width="90%" alt="Scatter plot for Documentary IMDB scores" />
</p>

---

### 3. How many unique categories does the Genre column have and how are they distributed?
- **Finding:** Over 50 unique genre classifications were identified. Documentaries, Dramas, and Comedies dominate the catalog, representing over 65% of all production volume.
<p align="center">
  <img src="https://github.com/user-attachments/assets/42dbfb5e-8c85-461b-8aa0-b83788a66dcb" width="90%" alt="Bar graph of Genre Distribution" />
</p>

---

### 4. What are the Top 3 most used languages in Netflix Originals?
- **Finding:** **English** is the dominant production language (>70%), followed by **Hindi** and **Spanish**, reflecting Netflix's strategic expansion into high-growth South Asian and Latin American streaming markets.
<p align="center">
  <img src="https://github.com/user-attachments/assets/87044b17-0a17-4e9b-b7d6-cbb7245a650f" width="80%" alt="Top 3 Languages Bar Graph" />
</p>

---

### 5. What are the Top 10 Netflix Originals by IMDB Rating?
- **Finding:** Critically acclaimed documentaries and cultural docuseries occupy 7 out of the top 10 positions on the platform.
<p align="center">
  <img src="https://github.com/user-attachments/assets/b56dc71c-3fcc-41d0-9b66-c9cd515fa988" width="90%" alt="Top 10 Movies by IMDB Ratings" />
</p>

---

### 6. What is the correlation between IMDB Score and Film Runtime?
- **Finding:** A mild positive correlation exists up to ~110 minutes, after which ratings plateau or decline. Films between **90 and 110 minutes** occupy the critical "sweet spot."
<p align="center">
  <img src="https://github.com/user-attachments/assets/c597551f-00ad-438f-bc76-7aff91536b95" width="85%" alt="Correlation between Score and Runtime" />
</p>

---

### 7. What are the Top 10 Genres by average IMDB Score?
- **Finding:** Specialized niche categories—including Documentary, Concert Films, and Historical Biographies—score significantly above mass-market comedies and horror films.
<p align="center">
  <img src="https://github.com/user-attachments/assets/80cf7b5c-31e8-4407-baa0-eb7014224941" width="85%" alt="Top 10 Genres by IMDB" />
</p>

---

### 8. What are the Top 10 Movies with the highest Runtime?
- **Finding:** Outlier productions reach up to 200+ minutes (anthologies, director's cuts, and regional epics).
<p align="center">
  <img src="https://github.com/user-attachments/assets/d36e76fe-a2dc-4974-9b65-76c2a0c326ad" width="80%" alt="Top 10 Highest Runtime Movies" />
</p>

---

### 9. In which year were the most Netflix Originals released?
- **Finding:** Annual production volume grew exponentially from 2015 to a historic peak in **2020**, before production cadence stabilized due to supply adjustments in 2021.
<p align="center">
  <img src="https://github.com/user-attachments/assets/a805687f-f35d-4855-a81b-526be7b91470" width="90%" alt="Released Genre per Year" />
</p>

---

### 10. Which language films have the lowest average IMDB ratings?
- **Finding:** Certain experimental or localized releases suffered from lower sample sizes and mixed reviews, highlighting opportunities for improved local script development.
<p align="center">
  <img src="https://github.com/user-attachments/assets/7ce4ebbf-e9e9-47b4-8c10-ee4f2056fd15" width="85%" alt="Lowest Average Rating Languages" />
</p>

---

### 11. Which year generated the greatest total content runtime?
- **Finding:** **2020** recorded the highest cumulative runtime across all releases, driven by Netflix's rapid response to global streaming demand surges.
<p align="center">
  <img src="https://github.com/user-attachments/assets/89951ac9-e5a0-43eb-a6ad-d4c8f62abe19" width="80%" alt="Greatest Total Runtime Year" />
</p>

---

### 12. Outlier Detection & Anomaly Analysis
- **Finding:** Box plot and IQR analysis identified extreme runtime outliers (<30 min short-form specials and >180 min multi-part releases) and rating distributions, allowing for cleaned subgroup modeling.
<p align="center">
  <img src="https://github.com/user-attachments/assets/a5b5ab19-2678-4b76-a505-83b5acec602a" width="90%" alt="Outlier Detection Scatter Plot" />
</p>

---

## 🚀 How to Run This Project

1. **Clone the repository:**
   ```bash
   git clone https://github.com/TAYAB-HUB/Netflix-Data-Analysis.git
   cd Netflix-Data-Analysis
   ```

2. **Install required dependencies:**
   ```bash
   pip install pandas numpy matplotlib seaborn plotly jupyter
   ```

3. **Execute ETL / Data Script (Optional):**
   ```bash
   python data/NetflixOriginals.py
   ```

4. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook "Notebook/Netflix Data for Exploratory Data Analysis.ipynb"
   ```

---

## 💡 Strategic Business Recommendations

1. **Target the 90–110 Minute Runtime Sweet Spot:** Data proves that viewer engagement and high critical scores peak within this window. Longer feature films must justify added production budgets with proven IP.
2. **Double-Down on High-ROI Documentary Production:** Documentaries deliver consistently higher average IMDB scores at a fraction of the production cost of CGI-heavy blockbusters.
3. **Expand Localized International Content:** With Hindi and Spanish emerging as key growth pillars, localized original storytelling provides high subscriber acquisition in competitive foreign markets.
4. **Shift from Volume-Centric to Quality-Informed Pipeline:** After the 2020 volume peak, the focus must be directed toward curated, high-reception titles rather than pure catalog volume.

---

## 👤 Author & Contact

**Syed Mohammed Tayab**  
- **Email:** [syedtayab01@gmail.com](mailto:syedtayab01@gmail.com)  
- **LinkedIn:** [linkedin.com/in/syedtayab01](https://www.linkedin.com/in/syedtayab01)  
- **GitHub:** [github.com/TAYAB-HUB](https://github.com/TAYAB-HUB)  
