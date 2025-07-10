# Earthquake-forecasting
# Earthquake Forecasting 

This repository contains data, code, and analysis for forecasting earthquakes in different tectonic zones of the Indian subcontinent. The study involves statistical modeling of inter-event times, regionalization of seismic zones, and visualization of seismicity including focal mechanisms.

---

## 🧭 Workflow Overview

1. **Raw Data Collection**
   - **Source**: [USGS Earthquake Catalog](https://earthquake.usgs.gov/earthquakes/search/)
   - **Format**: CSV (containing magnitude, latitude, longitude, depth, date, etc.)

2. **Data Preprocessing**
   - **Homogenization (to Moment Magnitude, Mw)**: Magnitudes are converted to a consistent scale (Mw) using empirical relationships.
   - **Aftershock Removal**: Declustering is applied to retain only mainshock events using temporal and spatial filtering criteria.

3. **Zonation of Seismic Regions**  
   Earthquake data is categorized into **six tectonic zones**:
   - Eastern Himalayan Arc  
   - Western Himalayan Arc  
   - Hindukush Region  
   - Indo-Burma Subduction Zone  
   - Andaman Region  
   - Kirthar-Sulaiman Region  

   Each region is exported as a separate CSV file for further individual analysis.

4. **Probability Estimation & Modeling**  
   For each region:
   - Inter-event times are computed.
   - Statistical distributions fitted:
     - **Exponential**
     - **Lognormal**
     - **Weibull**
     - **Gamma**
   - Model parameters estimated using **Maximum Likelihood Estimation (MLE)**.
   - Best-fit model selected using **Akaike Information Criterion (AIC)**.
   - **Conditional probabilities** are computed to estimate the likelihood of an event within a time window given the time since the last earthquake.

5. **Focal Mechanism Plotting**  
   Beachball diagrams are created for selected events using strike, dip, and rake values to visualize the nature of faulting (normal, reverse, strike-slip).

---



