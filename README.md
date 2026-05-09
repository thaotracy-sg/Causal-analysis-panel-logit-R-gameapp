📱 Mobile Game App Downloads — Panel Data Analysis
Fixed Effects & Random Effects Models | R · plm · ggplot2

Academic project completed as part of the ANL553 Applied Statistical Methods
and Causal Analysis module at Singapore University of Social Sciences (SUSS), 2025.
All data used is provided as part of the course assignment.


📌 Overview
This project investigates what drives weekly downloads of mobile game apps
using an unbalanced panel dataset of 16 apps observed over 56–72 weeks
(996 total observations).
Two panel data models are estimated and compared to identify the key factors
influencing app download behaviour in the mobile gaming market.

❓ Research Question

Which time-varying and time-invariant factors significantly influence
the weekly download count of mobile game apps?


📂 Repository Structure
game-app-panel-analysis/
│
├── Part1_GameApp_Panel_Analysis.Rmd   ← Full analysis (R Markdown)
├── Part1_GameApp_Panel_Analysis.html  ← Rendered report (open in browser)
└── README.md

🔬 Methods
StepMethodPurpose1Panel data structuring (pdata.frame)Define AppID × Week panel2Variable classificationIdentify time-varying vs time-invariant3Fixed Effects Model (plm, within)Control for app-specific unobservables4Robust standard errors (vcovHC)Correct for heteroskedasticity5Random Effects Model (plm, random)Include time-invariant predictors6Hausman Test (phtest)Determine preferred model statistically7Coefficient & residual visualisationInterpret and validate results

📊 Key Findings
VariableEffectSignificanceAvgPrice−195 to −213 downloads per $1 increase✅ Significant (p < 0.05)AvgInAppPur+1.49 downloads per unit✅ Significant (p < 0.001)Free.or.Paid−565 downloads for paid apps⚠️ Marginal (p = 0.064)WeeklyAvgRatingNo significant short-term effect❌ Not significantUpdateNo immediate download lift❌ Not significant

Preferred model: Random Effects (Hausman test p = 0.198 → fail to reject H₀)
Model fit: R² = 0.631 — explains 63% of download variation
Panel structure: 21% between-app variation, 79% within-app week-to-week


💡 Business Implications

Pricing strategy is critical — even a $1 increase significantly reduces downloads
In-app engagement drives downloads — monetisation and popularity reinforce each other
Weekly rating changes don't matter short-term — users rely on long-term reputation
App updates alone don't boost downloads — need to pair with marketing activity


🛠️ Tools & Packages
ToolPurposeRCore analysis languageplmPanel data modelling (FE & RE)lmtest + sandwichRobust standard errorsbroomTidy model outputsggplot2Coefficient plots, residuals, visualisationsdplyr + tidyrData wrangling

📈 How to Run

Clone this repository
Open Part1_GameApp_Panel_Analysis.Rmd in RStudio
Update the file path in the load-data chunk to your local data location
Click Knit to render the HTML report

Or simply open Part1_GameApp_Panel_Analysis.html in your browser to view
the full rendered analysis without running any code.

🔗 Related Projects

🌿 Sustainable Brand Choice — Binary Logit Analysis
🔋 Electric Power & CO₂ Forecasting
