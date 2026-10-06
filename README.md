# 🚨 Los Angeles Crime Data Exploratory Analysis (EDA)

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Plotly](https://img.shields.io/badge/Plotly-Interactive-3F4F75?logo=plotly)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-3776AB)
![Status](https://img.shields.io/badge/Status-Completed-success)

> An end-to-end exploratory data analysis of crime occurrences in Los Angeles, identifying temporal crime spikes, high-risk geographic sectors, and demographic victim profiles to provide actionable public safety insights.

---

## 📌 Project Overview & Objectives

Understanding crime trends is crucial for public safety resource allocation, urban planning, and emergency response optimization. This project examines historical crime incident records to answer core questions:
1. **Temporal Patterns:** What times of day experience the highest frequency of criminal incidents?
2. **Nighttime Hotspots:** Which geographic areas report the most incidents during high-vulnerability hours (10:00 PM – 3:59 AM)?
3. **Victim Profiles:** What are the age, gender, and descent distributions among reported victims?
4. **Modus Operandi & Weapons:** What weapons and crime classifications are most frequently documented?

---

## 📊 Key Findings & Business Insights

- **🕒 Peak Crime Hour:** Criminal activity shows a steady climb throughout the afternoon, peaking sharply during late afternoon/evening hours (around **18:00 - 20:00**).
- **🌙 Nighttime Risk Concentration:** Crimes between 10:00 PM and 4:00 AM are heavily clustered in specific urban areas (e.g., Central, 77th Street, and Hollywood divisions), highlighting areas in need of prioritized nighttime patrols.
- **👤 Demographic Trends:** Filtering out invalid records (ages $\le 0$ or sentinel values like $99$) reveals that young adults (ages 20–35) represent the most vulnerable demographic group.
- **🛠️ Weapon Utilization:** Non-firearm physical altercations and hands-on assaults constitute a large percentage of reported disputes alongside firearm-related incidents.

---

## 🛠️ Tech Stack & Methodologies

| Category | Tools / Techniques |
| :--- | :--- |
| **Language** | Python 3.x |
| **Data Manipulation** | `pandas`, `numpy` |
| **Data Visualization** | `seaborn`, `matplotlib`, `plotly.express`, `plotly.graph_objects` |
| **Techniques** | Data Cleansing, Imputation, Feature Engineering, Outlier Removal, Distribution Analysis |

---

## 🧹 Data Cleaning & Preprocessing Pipeline

1. **Handling Missing Values:**
   - Missing victim sex (`Vict Sex`) and weapon descriptions (`Weapon Desc`) were labeled as `"Unknown"`.
   - Missing victim descent codes (`Vict Descent`) were imputed using the distribution mode.
2. **Feature Engineering:**
   - Engineered `hour_occ` from military time `TIME OCC // 100` to standardize temporal hourly binning ($0$ through $23$).
3. **Anomaly & Outlier Filtering:**
   - Filtered out anomalous and corrupted age entries (`Vict Age <= 0` and code `99`).

---

## 📈 Visualizations Included

- **Hourly Crime Distribution:** Line chart with peak-hour indicator marking the maximum incident hour.
- **Top 10 High-Risk Areas at Night:** Horizontal bar chart displaying incident frequency during late-night hours.
- **Demographic Breakdown:** Age distribution histograms and gender-frequency plots.

---

## 💻 How to Run the Analysis Locally

### 1. Clone the repository
```bash
git clone https://github.com/mo010686/crime-data-.git
cd crime-data-
```

### 2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn plotly jupyter
```

### 3. Launch Jupyter Notebook
```bash
jupyter notebook "crime data in vs code.ipynb"
```

---

## 👤 Author
**Mohamed Hamdy**
- GitHub: [@mo010686](https://github.com/mo010686)
- LinkedIn: [Mohamed Hamdy](https://linkedin.com/in/YOUR-LINKEDIN-USERNAME)
