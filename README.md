Interactive effect of pre- and post-birth heat exposure on under-five mortality in sub-Saharan Africa

# Overview
This study aims to enhance understanding of the effects of pre- and post-birth heat exposure on under-five mortality in sub-Saharan Africa. Using a family-based case-control approach with data from 29 countries, the research controls for household-level confounding factors and explores various analytical models to assess heat exposure effects on child mortality and pregnancy loss.

# Research Objectives
1. Main Model: Evaluate the association between monthly heat days and under-five mortality.
2. Interaction Model: Assess the modification effect of gestational heat exposure.
3. Heterogeneity Analysis: Examine differences in gestational heat effects by gender and regional heat frequency.
4. Nonparametric Analysis: Explore nonlinear effects of heat exposure and test the hypothesis of in-utero selection.

# Software Requirements
R Statistical Software 4.1.0

# Data Sources
1. Health Data
Source: DHS Program (Demographic and Health Surveys)
Files: Birth's Recode (BR) files and Individual Recode (IR) files
Content: Monthly records of children's survival status and pregnancy outcomes
Access: [DHS Program](https://dhsprogram.com/)
2. Meteorological Data
Source: ERA5 ([Copernicus Climate Change Service](https://climate.copernicus.eu/))
Datasets:
Monthly data (0.25° × 0.25° resolution): Temperature, relative humidity, precipitation.
Daily data (0.25° × 0.25° resolution): Temperature.
Access: Copernicus Climate Change Service
3. Air Pollution Data
Source: EAC4 (Copernicus Atmosphere Monitoring Service)
Datasets: Monthly data (0.75° × 0.75° resolution):SO₂, NO₂, CO, PM₂.₅, and PM₁₀.
Access: [Copernicus Atmosphere Monitoring Service](https://ads.atmosphere.copernicus.eu/)

# Project Structure
The analysis pipeline consists of four steps:
1. Data Extraction
DHS-child.Rmd: Extract child survival data from DHS.
DHS-pregnancy.Rmd: Extract pregnancy loss data from DHS.
2. Geospatial Data Processing
DHS-GPS-weather.Rmd: Extract DHS GPS coordinates and match with meterological and air pollution data.
3. Data Integration
Combine dataset.Rmd: Merge processed health, meterological, and pollution datasets.
4. Modeling
Model.Rmd: Execute regression analysis, including main models, interaction models, heterogeneity analysis, and nonparametric models.
