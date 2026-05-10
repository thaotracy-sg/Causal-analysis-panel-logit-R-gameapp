# 📱 Mobile Game App Downloads — Panel Data Analysis
### Fixed Effects & Random Effects Models | R · plm · ggplot2

> **Academic project** completed as part of the ANL553 Applied Statistical Methods
> and Causal Analysis module at Singapore University of Social Sciences (SUSS), 2025.
> All data used is provided as part of the course assignment.

---

## 📌 Overview

This project investigates **what drives weekly downloads** of mobile game apps
using an unbalanced panel dataset of **16 apps observed over 56–72 weeks**
(996 total observations).

Two panel data models are estimated and compared to identify the key factors
influencing app download behaviour in the mobile gaming market.

---

## ❓ Research Question

> *Which time-varying and time-invariant factors significantly influence
> the weekly download count of mobile game apps?*
---

## 🔬 Methods

| Step | Method | Purpose |
|---|---|---|
| 1 | Panel data structuring (`pdata.frame`) | Define AppID × Week panel |
| 2 | Variable classification | Identify time-varying vs time-invariant |
| 3 | Fixed Effects Model (`plm`, `within`) | Control for app-specific unobservables |
| 4 | Robust standard errors (`vcovHC`) | Correct for heteroskedasticity |
| 5 | Random Effects Model (`plm`, `random`) | Include time-invariant predictors |
| 6 | Hausman Test (`phtest`) | Determine preferred model statistically |
| 7 | Coefficient & residual visualisation | Interpret and validate results |

---

## 📊 Key Findings

| Variable | Effect | Significance |
|---|---|---|
| **AvgPrice** | −195 to −213 downloads per $1 increase | ✅ Significant (p < 0.05) |
| **AvgInAppPur** | +1.49 downloads per unit | ✅ Significant (p < 0.001) |
| **Free.or.Paid** | −565 downloads for paid apps | ⚠️ Marginal (p = 0.064) |
| **WeeklyAvgRating** | No significant short-term effect | ❌ Not significant |
| **Update** | No immediate download lift | ❌ Not significant |

- **Preferred model:** Random Effects (Hausman test p = 0.198 → fail to reject H₀)
- **Model fit:** R² = 0.631 — explains 63% of download variation
- **Panel structure:** 21% between-app variation, 79% within-app week-to-week

---

## 💡 Business Implications

- **Pricing strategy is critical** — even a $1 increase significantly reduces downloads
- **In-app engagement drives downloads** — monetisation and popularity reinforce each other
- **Weekly rating changes don't matter short-term** — users rely on long-term reputation
- **App updates alone don't boost downloads** — need to pair with marketing activity

---

## 🛠️ Tools & Packages

| Tool | Purpose |
|---|---|
| `R` | Core analysis language |
| `plm` | Panel data modelling (FE & RE) |
| `lmtest` + `sandwich` | Robust standard errors |
| `broom` | Tidy model outputs |
| `ggplot2` | Coefficient plots, residuals, visualisations |
| `dplyr` + `tidyr` | Data wrangling |

---

## 📈 How to Run

1. Clone this repository
2. Open `Part1_GameApp_Panel_Analysis.Rmd` in RStudio
3. Update the file path in the `load-data` chunk to your local data location
4. Click **Knit** to render the HTML report

Or simply open `Part1_GameApp_Panel_Analysis.html` in your browser to view
the full rendered analysis without running any code.

---

## 🔗 More Projects

📊 [Power BI IMS Dashboard Enhancement – Healthcare](https://github.com/thaotracy-sg/powerbi-ims-dashboard-enhancement-healthcare) <br>
🛒 [SQL + R Customer Survey Pipeline](https://github.com/thaotracy-sg/sql-r-customer-survey-pipeline) <br>
🌿 [Sustainable Brand Logit Analysis](https://github.com/thaotracy-sg/Sustainable-brand-logit-analysis) <br>
🧴 [Commercial Analytics – Skincare Channel Performance](https://github.com/thaotracy-sg/Commercial-analytics-skincare-channel-performance) <br>
🔋 [Time Series Forecasting – Electric Power & CO2 Emissions](https://github.com/thaotracy-sg/Time-series-forecasting-electric-power-co2-emission-europe) <br>

---

*Analysis by Tracy Nguyen | ANL553 Applied Statistical Methods & Causal Analysis | SUSS 2025*
