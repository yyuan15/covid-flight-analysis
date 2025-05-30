# ✈️ COVID Impact on U.S. Flight Behavior

This project explores the impact of the COVID-19 pandemic on flight volumes at the five busiest U.S. airports in 2019: ATL (Georgia), LAX (California), DEN (Colorado), DFW (Texas), and ORD (Illinois). It examines the severity and pace of recovery in air travel throughout 2020 using both airline data and state-level COVID-19 case data.

## 🔍 Research Questions

1. **How did the COVID-19 pandemic impact total flights in the five top airports in 2020 compared to 2019?**

2. **How did flight volumes correlate with the rise in COVID-19 cases in the five corresponding states in 2020?**

3. **Which airports/states demonstrated the strongest recovery, and how can we quantify "resilience" in flight behavior?**

---

## 📁 Data Sources

- **Flight Data**: `Top5airportsUS.csv`  
  Contains ~2.5M rows of flight records from the five busiest U.S. airports (2019–2020).

- **COVID Data**: `Top5StateCovid.csv`  
  Contains daily state-level COVID-19 statistics for GA, CA, CO, TX, and FL throughout 2020.

---

## 📊 Methodology

### ➤ Data Wrangling
- Cleaned and filtered flight data for 2019 and 2020.
- Aggregated monthly flight volumes by state.
- Aligned COVID-19 case data with flight data by matching month-end positive case counts.

### ➤ Visualization
- Created bar plots and time-series line plots comparing:
  - Flight volume change (2019 vs 2020)
  - Monthly flights vs. COVID-19 cases (2020)
- Used faceted plots to highlight state-level trends.

### ➤ Quantitative Analysis
- Constructed a **Resilience Score** = (1 / Months to Recover to 80%) × (100 + Dropped Percentage)
  - **Months to Recover to 80%**: Number of months it took for flight volume to recover to 80% of pre-COVID levels.
  - **Dropped Percentage**: Percentage drop in flight volume.
- Used this score to rank state performance in terms of recovery strength and speed.

---

## 📌 Key Findings

- All five airports saw significant flight reductions in 2020. The largest percentage drops occurred at **ORD** and **LAX**.
- **DEN (Colorado)** showed the most rapid and robust recovery, even exceeding March 2020 flight levels by August.
- Flight volume and COVID-19 cases were **positively correlated** in CO, TX, and GA — indicating recovery occurred despite rising case counts.
- The **Resilience Score** metric effectively captured the dual dimensions of recovery: **depth of drop** and **speed of rebound**.

---


## 🧪 Reproducibility

To replicate this project:

1. Clone the repo:
   ```bash
   git clone https://github.com/yyuan15/covid-flight-analysis.git
2. Open the .Rmd file in RStudio or VS Code with the R extension.
3. Install the required packages:
   ```r
   install.packages(c("dplyr", "ggplot2", "lubridate", "tidyverse"))
   ```

