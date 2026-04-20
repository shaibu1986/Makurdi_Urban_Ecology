# Elucidating the Urbanization Filter in Makurdi, Nigeria

This repository contains the geospatial datasets, machine learning models, and analytical workflows for the study assessing edaphic constraints and vegetation resilience along an anthropogenic gradient in Makurdi, Nigeria.

## 👥 Authors
* **Shaibu Ochoche** — Peoples' Friendship University of Russia (RUDN).
* **Anatoly Aleksandrovich Kirichuk** — Peoples' Friendship University of Russia (RUDN).
* **Emaikwu Patience Onyamoche** — Sechenov First Moscow State Medical University.

## 📝 Abstract
Urbanization fundamentally alters the abiotic filters that govern vegetation health, yet the specific geochemical thresholds of these transitions remain poorly understood in tropical Guinea-Savannah cities. This study characterizes the environmental filtering process in Makurdi, Nigeria, by integrating satellite-derived anthropogenic and biological indices with high-resolution edaphic data. Utilizing a Random Forest regressor and Partial Dependence Modeling, we analyzed the hierarchical influence of urbanization intensity and eight soil biophysical properties on the Enhanced Vegetation Index (EVI). 

The model demonstrated exceptional predictive power ($R^2 = 0.914$; $RMSE = 0.0135$), identifying **Soil Organic Carbon (SOC)** as the "Master Filter" of the landscape. A significant urban geochemical signature was observed, where increased urbanization intensity was positively coupled with soil alkalinity ($r = 0.249, p < 0.001$), creating a physiological bottleneck for native flora. Critical ecological tipping points were established at an **SOC median of 11.27 g/kg** and a **pH of 5.77**, below which vegetation vigor undergoes rapid non-linear decline.

## 📊 Key Results
* **Model Performance:** $R^2 = 0.914$ (Random Forest Regressor).
* **Dominant Filter:** Soil Organic Carbon (SOC) is the primary driver of vegetation vigor.
* **Ecological Tipping Points:**
    * **SOC:** 11.27 g/kg
    * **pH:** 5.77
    * **Bulk Density:** 1.37 g/cm³

## 📂 Repository Structure
* `/data`: Final processed CSV dataset extracted from Google Earth Engine.
* `/scripts/GEE`: JavaScript code for VIIRS and Sentinel-2 data fusion.
* `/scripts/Python`: Jupyter Notebooks for Random Forest and PDP threshold detection.
* `/figures`: High-resolution versions of Figures 1–9.

---

## 🛠️ Replication and Peer-Review Protocol
To verify the analytical integrity of this study, kindly follow this two-stage validation process:

### **Stage 1: Geospatial Extraction (GEE)**
First, execute the **Google Earth Engine (GEE)** script provided in:  
`scripts/GEE/Data_Extraction.js`

This step enables direct observation of the multi-sensor data fusion (Sentinel-2, VIIRS NTL, and SoilGrids 2.0) and the systematic 500m grid-based sampling process used to generate the study dataset.

### **Stage 2: Analytical Validation (Colab)**
Once the data origin is verified, launch the master notebook using the badge below:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shaibu1986/Makurdi_Urban_Ecology/blob/main/Makurdi_Urban_Environmental_Filter_Analysis.ipynb)

**File Path:** `scripts/Python/Makurdi_Urban_Environmental_Filter_Analysis.ipynb`

By launching this notebook, the environment will automatically clone the repository and utilize the synchronized datasets in the `/data` folder to reproduce all statistical results, machine learning rankings, and ecological thresholds ($R^2 = 0.914$) exactly as reported in the manuscript.

---

## ⚖️ License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
