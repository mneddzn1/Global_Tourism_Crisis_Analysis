# 🇪🇬 Egypt's Tourism Under Fire

**Measuring the Impact of Crises on Visitor Arrivals (1995 to 2019)**

> A data analysis project for the Data Analysis course at Egypt University of Informatics (Spring 2026)

---

## 📌 About

This project investigates how major political and security crises affected tourism in Egypt over 25 years. Using real World Bank data, we measure the exact percentage drops, compare Egypt with its MENA neighbors, and use hypothesis testing to prove the drops are statistically significant.

## 👥 Team

| Name | ID |
|---|---|
| Mostafa Elnagar | 24-101443 |
| Yousef Eslam | 24-101303 |
| Ahmed Sami | 24-101314 |
| Adham Shams | 24-101192 |

## 📂 Project Structure

```
P 3/
├── Proejct/
│   ├── ready to submit Project/
│   │   ├── Global_Tourism_Crisis_Analysis.ipynb   # Main notebook (code + analysis)
│   │   ├── Final_Report.docx                      # Final report (professor template)
│   │   ├── Final_Report.pdf                       # Final report (PDF version)
│   │   └── Charts/                                # Exported chart images
│   │       ├── 1.chart.png                        # Crisis comparison bar chart
│   │       ├── 2.chart.png                        # Tourism timeline (1995 to 2019)
│   │       ├── 3.chart.png                        # MENA regional comparison
│   │       └── 4.chart.png                        # Stable vs Turbulent boxplot
│   └── YT video linnks.txt                        # YouTube sources for extra techniques
├── Proposal_P3_v2.0.pdf                           # Project proposal
├── Course materials/                              # Lecture slides and references
└── README.md
```

## 📊 Dataset

| File | Source | Description |
|---|---|---|
| `arrival_data.csv` | [World Bank](https://data.worldbank.org) | International tourist arrivals per country (1960 to 2024) |
| `income_categories.csv` | World Bank | Country metadata (region, income group) |

Indicator used: **ST.INT.ARVL** (International tourism, number of arrivals)

## 🔍 Research Questions

1. **The Biggest Hit** — Which crisis caused the worst single year drop?
2. **The Comeback Time** — How long does recovery take?
3. **The Neighborhood Effect** — Do Morocco, Tunisia, and Jordan get hit the same way?
4. **The Hidden Pattern** — Are the crisis drops statistically significant?

## 🔬 Key Findings

| Metric | Value |
|---|---|
| Peak arrivals | **14.7M** (2010) |
| Worst drop | **-42.1%** (Sinai Plane Crash, 2016) |
| Arab Spring drop | **-33.2%** (2011) |
| T-statistic | **3.7622** |
| P-value | **0.0011** |
| Result | **Reject H0** — crisis drops are statistically significant |

## 🛠 Tools and Libraries

- **pandas / numpy** — data cleaning, reshaping (melt), YoY percentage change
- **matplotlib** — annotated timeline plots, bar charts
- **seaborn** — whitegrid theme, consistent styling
- **scipy.stats** — independent two sample t-test (ttest_ind)

## ▶️ How to Run

1. Clone this repo
2. Make sure you have Python 3.x with the required libraries:
   ```
   pip install pandas numpy matplotlib seaborn scipy
   ```
3. Open `Global_Tourism_Crisis_Analysis.ipynb` in Jupyter or VS Code
4. Click **Run All**

## 📎 Extra Techniques (learned from YouTube)

| Technique | What it does |
|---|---|
| `plt.axhline()` | Draws a zero baseline for easy visual comparison |
| `sns.set_theme()` | Applies a clean whitegrid style to all charts |
| `plt.axvspan()` | Shades a time period (used to highlight the Arab Spring) |
| Dynamic labeling with `enumerate()` | Puts exact numbers directly on chart bars |
