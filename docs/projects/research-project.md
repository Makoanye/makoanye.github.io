<!--
CHECKLIST FOR THIS PAGE (copy this file for each new project):
- [ ] Replace [YOUR PROJECT TITLE] with your project title
- [ ] Replace the hero image with your own (add to docs/assets/images/)
- [ ] Update the Overview section
- [ ] Update the Methods & Tools section
- [ ] Update the Key Findings section
- [ ] Update the Links section
- [ ] Add a card for this project on docs/projects/index.md
- [ ] Add a nav entry in mkdocs.yml
-->

# Impacts of Climate Change on Streamflow and Hydrological Extremes in the South Phuthiatsana Catchment — MSc Dissertation, *National University of Lesotho (2025)*

![Project overview image](../assets/images/placeholder-project.jpg)

## Overview

This study assessed how climate change is affecting streamflow variability and hydrological extremes in the South Phuthiatsana Catchment, Lesotho. I used the SWAT+ hydrological model alongside an XGBoost machine learning model to simulate streamflow and project future scenarios, drawing on locally sourced streamflow and climate records (rainfall, temperature, humidity, and wind), DEM, soil, and land use/land cover data, supplemented with the C3S ERA5 reanalysis dataset. The research identified key trends and risks to water resources under changing climate conditions, generating actionable insights to support integrated water resources management and climate adaptation planning in the catchment.

**Study Area:** South Phuthiatsana Catchment  
**Duration:** January 2025 – June 2025  
**Role:** Thesis  
**Status:** Completed

---

## Methods & Tools

**Data Sources**

- Streamflow - Department of Water Affairs
- Climate Data Lesotho Meteorological Services
- Soil Map Layers - FAO
- Land Use / Land Cover - ESRI LULC 2024
- DEM - USGS
- 

**Processing Steps**

1. Compiled and quality-checked historical climate (rainfall, Tmax, Tmin, humidity, wind) and streamflow data (1973–2014), and tested for trends using the Mann-Kendall test and Sen's slope estimator.
2. Bias-corrected MPI-ESM1-2-LR (CMIP6) GCM outputs using linear scaling (precipitation) and quantile mapping (temperature) to generate reliable climate projections for SSP2-4.5 and SSP5-8.5 scenarios (2041–2080).
3. Built and calibrated a SWAT+ hydrological model using sensitivity analysis (7 key parameters) and water balance checks; after it underperformed (NSE < 0.5), trained an XGBoost model on historical streamflow and climate data instead.
4. Used the validated XGBoost model to simulate future daily streamflow under both climate scenarios, then analyzed hydrological extremes via flow duration curves, flow frequency analysis, and quantile/regime shifts.

**Tools Used**

| Tool | Purpose |
|------|---------|
| SWAT+ | Physically-based hydrological modeling and water balance |
| XGBoost(Python) | Machine LEarning-based streamflow simulation and future projection |
| R/Python(Mann-Kendall, Sen's Slope) | Statistical trend analysis of climate and streamflow data |
| C3S ERA5/CMIP6 (MPI-ESM1-2-LR) | Climate reanalysis and GCM projection data sourcing |


---
## Key Findings

- Historical temperatures show statistically significant warming (Tmax +0.035°C/yr, Tmin +0.019°C/yr, 1984–2014), with further warming of 1.56–1.91°C projected by 2061–2080 under SSP2-4.5/SSP5-8.5
- SWAT+ underperformed for streamflow simulation (NSE = 0.17–0.20), so XGBoost was adopted instead, achieving strong accuracy (NSE = 0.89 training, 0.62 validation).
- Future projections show a major hydrological regime shift: extreme high flows (floods) are projected to decline by over 50%, while low flows are projected to rise substantially (e.g., Q1 flow increasing from near-zero to ~9.0 m³/s), pointing to reduced flood risk but a more frequent, moderate low-flow regime requiring adaptive water management.


---

## Links

[View Code on GitHub](https://github.com/[YOUR-GITHUB-USERNAME]/[YOUR-REPO-NAME]){ .md-button }
[View Data Source](https://example.com){ .md-button }
