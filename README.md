# Climate Extreme Events Modelling

Statistical modelling of extreme precipitation events in Southern France using climate projections, Generalized Linear Models (GLM) and Extreme Value Theory (EVT).

---

## Project Overview

This project was developed as part of an actuarial research project on climate risk.

The objective is to analyse historical and projected climate data in order to:

- explore the spatial distribution of extreme precipitation;
- identify geographic areas exposed to higher frequencies of heavy rainfall;
- model precipitation intensity using Gamma Generalized Linear Models;
- estimate the behaviour of extreme rainfall through Peaks-Over-Threshold (POT) and Generalized Pareto Distribution (GPD) models.

The project combines exploratory data analysis, spatial visualisation and statistical modelling to study the occurrence and severity of extreme precipitation events.

---

## Data

The analysis uses climate data for Southern France composed of:

- historical observations;
- climate projections;
- daily precipitation;
- wind speed;
- temperature;
- geographic coordinates (latitude and longitude).

Historical precipitation is converted from **kg/m²/s** to **mm/day** before the analysis.

---

## Methodology

The project follows the workflow below.

### 1. Data preparation

- data cleaning;
- date conversion;
- precipitation unit conversion;
- creation of calendar variables;
- merging historical and projected datasets.

### 2. Exploratory Data Analysis

- precipitation time series;
- precipitation distribution;
- annual and monthly summaries;
- threshold exceedance analysis.

### 3. Spatial Analysis

Interactive Leaflet maps are used to visualise the spatial distribution of extreme precipitation.

Geographic locations are segmented according to the average annual number of threshold exceedances.

### 4. Gamma Generalized Linear Models

Positive precipitation amounts are modelled using Gamma GLMs.

Candidate models are compared through:

- 10-fold cross-validation;
- RMSE;
- AIC;
- BIC.

### 5. Extreme Value Theory

Extreme precipitation is analysed using a Peaks-Over-Threshold approach.

The project includes:

- Mean Residual Life plots;
- Threshold Choice plots;
- Stationary Generalized Pareto models;
- Non-stationary GPD models with time-varying scale parameters.

---

## Main Results

The analysis highlights:

- strong spatial heterogeneity in extreme precipitation;
- locations exhibiting higher frequencies of threshold exceedances;
- the usefulness of Gamma GLMs for modelling strictly positive precipitation;
- the relevance of EVT for characterising the tail behaviour of extreme rainfall.

---

## Repository Structure

```
.
├── climate_extreme_events.Rmd
├── README.md
├── data/
│   ├── historical_precipitation.txt
│   └── projected_precipitation.txt
├── outputs/
│   ├── figures/
│   └── tables/
└── renv.lock
```

---

## Technologies

- R
- dplyr
- data.table
- ggplot2
- leaflet
- extRemes
- POT
- lubridate

---

## Statistical Methods

- Exploratory Data Analysis
- Spatial Data Analysis
- Gamma Generalized Linear Models
- Cross-Validation
- Model Selection (RMSE, AIC, BIC)
- Extreme Value Theory
- Peaks Over Threshold (POT)
- Generalized Pareto Distribution (GPD)

---

## Reproducibility

Clone the repository and open the R Markdown notebook.

```r
install.packages("renv")
renv::restore()
```

Render the notebook with

```r
rmarkdown::render("climate_extreme_events.Rmd")
```

---

Actuary | Climate Risk | Statistical Modelling | Machine Learning
