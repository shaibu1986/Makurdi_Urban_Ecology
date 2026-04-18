# Elucidating the Urbanization Filter in Makurdi, Nigeria

This repository contains the geospatial datasets, machine learning models, and analytical workflows for the study assessing edaphic constraints and vegetation resilience along an anthropogenic gradient in Makurdi, Nigeria.

## 👥 Authors
* **Shaibu Ochoche** - Peoples' Friendship University of Russia (RUDN).
* **Emaikwu Patience Onyamoche** - Sechenov First Moscow State Medical University.
* **Anatoly Aleksandrovich Kirichuk** - Peoples' Friendship University of Russia (RUDN).

## 📝 Abstract
Urbanization fundamentally alters the abiotic filters that govern vegetation health, yet the specific geochemical thresholds of these transitions remain poorly understood in tropical Guinea-Savannah cities. This study characterizes the environmental filtering process in Makurdi, Nigeria, by integrating satellite-derived anthropogenic and biological indices with high-resolution edaphic data. Utilizing a Random Forest regressor and Partial Dependence Modeling, we analyzed the hierarchical influence of urbanization intensity and eight soil biophysical properties on the Enhanced Vegetation Index (EVI). The model demonstrated exceptional predictive power (R2 = 0.914; RMSE = 0.0135), identifying Soil Organic Carbon (SOC) as the "Master Filter" of the landscape, with an importance score nearly triple that of any other variable. A significant urban geochemical signature was observed, where increased urbanization intensity was positively coupled with soil alkalinity (r = 0.249, p < 0.001), creating a physiological bottleneck for native flora adapted to acidic Savannah soils. Critical ecological tipping points were established at an SOC median of 11.27 g/kg and a pH of 5.77, below which vegetation vigor undergoes rapid non-linear decline. These findings suggest that urban canopy resilience in Makurdi is primarily dictated by nutritional and chemical thresholds rather than soil physical structure. We propose a "soil-first" management framework that prioritizes the protection of riparian carbon hotspots and the use of organic amendments to maintain soils within "Safe Operating Spaces." These data-driven targets provide a reproducible methodology for ensuring urban ecological persistence amidst rapid expansion in Sub-Saharan Africa.

## 📊 Key Results
- **Model Performance:** $R^2 = 0.914$ (Random Forest Regressor).
- **Dominant Filter:** Soil Organic Carbon (SOC) is the primary driver of vegetation vigor.
- **Tipping Points:** - SOC: 11.27 g/kg
  - pH: 5.77
  - Bulk Density: 1.37 g/cm³

## 📂 Repository Structure
- `/data`: Final processed CSV dataset extracted from Google Earth Engine.
- `/scripts/GEE`: JavaScript code for VIIRS and Sentinel-2 data fusion.
- `/scripts/Python`: Jupyter Notebooks for Random Forest and PDP threshold detection.
- `/figures`: High-resolution versions of Figures 1–9.

## 💻 Usage
To reproduce the findings:
1. Access the Google Earth Engine script in `/scripts/GEE` to extract spatial layers.
2. Use the Python notebooks in `/scripts/Python` to run the regression and generate threshold plots.

## ⚖️ License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
