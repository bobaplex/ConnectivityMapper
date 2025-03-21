# Cell Tower Placement Optimization using Machine Learning

**Author**: Anagha Rao  
**Organization**: UW-GDA  
**Repository**: [ConnectivityMapper](https://github.com/bobaplex/ConnectivityMapper?tab=readme-ov-file)  

---

## Project Summary  
This project aims to optimize cell tower placement by leveraging machine learning to analyze terrain, connectivity gaps, and ROI. The goal is to identify locations that maximize coverage and user adoption while minimizing infrastructure costs, enabling smarter business decisions for telecom expansion.

---

## Background  
With the increasing demand for seamless connectivity, telecom companies face challenges in expanding coverage efficiently. Traditional methods for tower placement often overlook terrain constraints, user demand patterns, and cost-effectiveness. This project uses geospatial data, signal propagation models, and demographic insights to address these challenges.

---

## Problem Statement  
- **Objective**: Develop an ML model to recommend optimal cell tower locations based on terrain, connectivity, and ROI.  
- **Key Questions**:  
  - Where are the coverage gaps in existing networks?  
  - Which locations will maximize user adoption and ROI?  
  - How can terrain and infrastructure costs be factored into placement decisions?  

---

## Datasets  
1. **Terrain Data**: Elevation and land cover data from [OpenTopography API](https://opentopography.org/).  
2. **Connectivity Data**: Signal strength maps and tower locations from [FCC](https://www.fcc.gov/). Cellular data from [ARCGIS Hub](https://hub.arcgis.com/datasets/geoplatform::cellular-towers/explore?location=2.226280%2C-18.957773%2C1.50).  
3. **Demographics**: Population density (weighted and unweighted) from [WorldPOP Hub](https://hub.worldpop.org/geodata/summary?id=50575).  
4. **Infrastructure Costs**: Land prices and construction costs (to be sourced from public datasets or estimates).  

---

## Tools & Packages  
- **Python Libraries**:  
  - `geopandas` (geospatial data processing)  
  - `scikit-learn` (ML modeling)  
  - `rasterio` (terrain data analysis)  
  - `folium` (interactive maps)  
- **Other Tools**:  
  - Jupyter Notebooks for prototyping.  
  - GitHub for version control and collaboration.  

---

## Methodology  
1. **Data Collection**: Gather terrain, connectivity, and demographic datasets.  
2. **Feature Engineering**:  
   - Extract **elevation** and **slope** from DEM.  
   - Calculate **distance to nearest tower** and **coverage overlap**.  
   - Add **population density** (weighted and unweighted) and **income levels**.  
3. **Model Development**:  
   - Train an **XGBoost model** to predict **user demand** and **ROI**.  
   - Use **SHAP values** to interpret feature importance.  
4. **Optimization**:  
   - Rank potential tower locations based on predicted ROI and coverage.  
5. **Visualization**:  
   - Create **interactive maps** to showcase recommended placements.  
   - Generate **charts** comparing predicted ROI for different regions.  

---

## Results  
- **Optimal Tower Locations**: Identified top 5 locations with high predicted user demand and ROI.  
- **Improved Coverage**: Demonstrated how optimized placement can bridge coverage gaps in rural areas.  
- **Cost Savings**: Showed how data-driven decisions can minimize infrastructure costs.  

---

## Conclusions  
- The model successfully identifies **optimal tower locations** using geospatial and demographic data.  
- **Population density** and **terrain features** are the most important factors in predicting user demand.  

---

## Future Directions  
1. **Incorporate Additional Data**:  
   - Add **income data** to refine ROI predictions.  
   - Include **real-time data** (e.g., network usage, weather) for dynamic optimization.  
2. **Consumer-Centric Design**:  
   - Go beyond income and consider **consumer preferences** (e.g., data usage patterns, service expectations).  
3. **Expand Applications**:  
   - Apply the model to other industries, such as **IoT** or **smart city planning**.  

---

## References  
- [FCC Tower Data](https://www.fcc.gov/)  
- [USGS Terrain Data](https://www.usgs.gov/)  
- [Census Demographic Data](https://www.census.gov/)  
- Python Documentation for `geopandas`, `scikit-learn`, and `folium`.  

---

**Note**: This README will be updated as the project evolves.  
