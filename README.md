# US Gun Violence Data Analysis

---

## 📌 Overview
A comprehensive statistical analysis of US gun violence incidents from 
2014 to 2023, merging gun violence records with US Census state-level 
demographic data to explore temporal trends, geographic distribution, 
socioeconomic patterns, and incident severity across the United States.

---

## ❓ Research Question
**Is the average number of gun violence victims per incident higher in 
low-income states compared to high-income states?**

**Finding:** Yes — a Monte Carlo permutation test (5,000 permutations) 
confirmed a statistically significant difference (p < 0.05), indicating 
that low-income states experience more severe gun violence incidents on average.

---

## 📂 Datasets
| Dataset | Description |
|---|---|
| `gun_violence_geo.csv` |  Gun violence incidents Jan 2014 – Dec 2023 with geographic coordinates |
| `census_data_state_2008-2023.csv` | US Census ACS state-level estimates including population, income, and poverty rates |

---

## 🔍 Analysis Sections

**1. Data Dictionary & EDA**
- Variable descriptions, data types, and missingness visualization
- Faceted lollipop charts and upset plots for missing data patterns

**2. Data Cleaning & Merging**
- Merged gun violence data with Census data by State and Year
- String manipulation on address and city fields
- Date/time extraction for weekday and monthly trend analysis

**3. Visualizations**
- Total incidents by state (bar chart)
- Population vs. total victims (log-scaled scatterplot)
- Victims trend over time (line plot)
- Killed vs. injured by state (stacked bar chart)
- Top incident characteristics by state (grouped bar chart)
- Bubble chart of severity across top 10 states
- Interactive map of 500 sampled incidents (Leaflet)

**4. Statistical Inference**
- Monte Carlo Permutation Test (5,000 permutations)
- Bootstrap confidence intervals for mean incident severity

---

## 🛠️ Tools & Packages
| Category | Packages |
|---|---|
| Data Wrangling | `tidyverse`, `dplyr`, `tidyr`, `lubridate`, `stringr` |
| Visualization | `ggplot2`, `ggrepel`, `ggpubr`, `circlize`, `leaflet` |
| Tables | `gt`, `flextable`, `skimr` |
| Statistics | `boot`, `bootstrap` |
| Reporting | `Quarto`, `magick`, `naniar` |

---

## 📈 Key Findings
- Gun violence incidents show a consistent upward trend from 2014 to 2023
- High-population states report more total incidents but severity varies
- Low-income states have statistically significantly higher average victims per incident
- Weekday patterns reveal variation in when incidents occur
- Geographic clustering visible across Southern and Midwestern states

---

## 🚀 Live Report
👉 [View Live Report](https://kdeepr.github.io/US-gun-data-analysis-in-R/US_gun_data_Analysis.html)

---

## 📁 Repository Structure
├── US_gun_data_Analysis.qmd   # Main Quarto analysis file
├── gun_violence_geo.csv       # Primary dataset
├── .github/
│   └── workflows/
│       └── render.yml         # Auto-render GitHub Actions workflow
└── README.md

---

## ▶️ How to Run Locally
```r
# Install required packages
install.packages(c("readr","skimr","gt","dplyr","tidyr","ggplot2",
                   "stringr","scales","circlize","tidyverse","flextable",
                   "naniar","lubridate","ggpubr","magick","ggrepel",
                   "leaflet","boot","bootstrap"))

# Render the report
quarto render US_gun_data_Analysis.qmd
```


### A project in STA 518 — Grand Valley State University | Kuladeep Roy G
