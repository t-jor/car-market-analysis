## Car Market Analysis  
**Exploratory Data Analysis, Statistical Modeling & Insights**

## Overview
This project analyzes a car market dataset to explore pricing, fuel efficiency, and popularity patterns across passenger vehicles.  
The focus lies on descriptive analysis, robust data cleaning, and interpretable statistical methods rather than predictive modeling.

The analysis focuses on combustion-engine vehicles produced from 1995 onward to ensure comparability and sufficient data quality.

---

## Objectives
- Clean and standardize raw vehicle listing data
- Explore distributions and relationships of key technical attributes
- Assess pricing drivers using correlation and regression analysis
- Examine whether vehicle popularity differs across categorical characteristics
- Clearly distinguish statistical significance from practical relevance

---

## Dataset Context
- Each row represents a single vehicle listing
- The dataset includes technical vehicle attributes, pricing, fuel efficiency, and popularity metrics
- The dataset does **not** explicitly distinguish between new and used vehicles
- Variables such as mileage or vehicle condition are not available

---

## Analysis Structure

### Data Loading & Inspection
- Load data from a GitHub-hosted CSV for reproducibility
- Inspect structure, data types, missing values, and basic distributions

### Data Cleaning
- Handle missing values using domain-driven assumptions
- Introduce an explicit engine type classification (combustion, electric, rotary)
- Remove non-informative or structurally ambiguous features
- Standardize data types and string representations

### Filtering & Feature Engineering
- Restrict analysis to vehicles from model year 1995 onward
- Focus on combustion-engine vehicles for metric comparability
- Create derived features such as:
  - `total_mpg` (combined fuel efficiency)
  - `price_per_hp` (price–performance proxy)

### Exploratory Data Analysis (EDA)
- Descriptive statistics for key numerical variables
- Group-based comparisons across drivetrain, vehicle size, and engine configuration
- Visual analysis of distributions, outliers, and non-linear patterns

### Correlation & Regression Analysis
- Pearson correlation analysis with visual heatmaps
- Pairwise correlations with confidence intervals and p-values
- Linear regression models to assess the relationship between engine power and price

### ANOVA
- One-way ANOVA to test differences in vehicle popularity across vehicle sizes
- Post-hoc Tukey tests for pairwise group comparisons
- Visual validation using boxplots

---

## Key Findings
- Engine horsepower is the strongest technical predictor of vehicle price
- Fuel efficiency decreases as engine power and cylinder count increase
- Engine configuration adds only limited explanatory power beyond horsepower
- Vehicle popularity shows weak association with technical attributes
- Statistically significant popularity differences across vehicle sizes exist but are modest in practical magnitude

---

## Limitations
- Analysis is descriptive and relies on simplified linear models
- Extreme price outliers influence distributions and model fit
- Non-technical factors (brand positioning, design, market dynamics) are not explicitly modeled
- Results should not be interpreted causally

---

## Tools & Libraries
- Python (pandas, numpy)
- Visualization: matplotlib, seaborn
- Statistics & modeling: scipy, statsmodels, pingouin

---

## 🧑‍💻 Author

**Thomas Jortzig**  
 Vehicle Pricing, Efficiency & Popularity Analysis – Car Market Analysis (02/2026)

---

## Notes
This project emphasizes transparency, reproducibility, and interpretability over model complexity.  
All analytical decisions are explicitly motivated and documented in the notebook.
