# Environmental-Analysis-Using-Remote-Sensing-GIS-and-Machine-Learning-Amman-2023-
A data-driven environmental modeling project integrating Google Earth Engine, RSD, GIS datasets, and Machine Learning to analyze vegetation health (NDVI) across the Amman region, Jordan.

# 🌍 Environmental Analysis Using Remote Sensing, GIS, and Machine Learning (Amman 2023)

This project demonstrates how to integrate **Remote Sensing data**, **Geographic Information Systems (GIS)**, and **Machine Learning** to model and visualize environmental health indicators.  
The analysis focuses on the **Amman region (Jordan)** for the year **2023**, using the **Normalized Difference Vegetation Index (NDVI)** derived from Sentinel-2 imagery.

---

## 📊 Project Overview

This Jupyter Notebook connects to **Google Earth Engine (GEE)** to extract satellite and environmental data, then processes it using Python libraries such as `geemap`, `rioxarray`, `rasterio`, and `scikit-learn`.

The goal is to:
- Measure vegetation health using NDVI.  
- Integrate GIS layers such as **Elevation (SRTM)** and **Rainfall (CHIRPS)**.  
- Train a **Random Forest Regression** model to understand which environmental factors drive vegetation variation.  
- Visualize the results through static and interactive maps.

---

## 🧠 Key Steps Implemented

1. **Import & Authenticate Google Earth Engine**  
   Connects your Python environment with the Earth Engine API.

2. **Define Region of Interest (ROI)**  
   A bounding box covering the Amman region, Jordan.

3. **Download and Compute NDVI**  
   Uses Sentinel-2 Level-2A imagery for 2023 to calculate NDVI = (NIR – RED) / (NIR + RED).

4. **Add GIS Layers**  
   - Digital Elevation Model (DEM) from SRTM.  
   - Rainfall data from CHIRPS.

5. **Raster Alignment and Stacking**  
   All rasters are resampled and reprojected to the same spatial grid for modeling.

6. **Machine Learning Modeling**  
   Trains a `RandomForestRegressor` to predict NDVI using elevation and rainfall.

7. **Visualization & Results**  
   - NDVI heatmap with color scale.  
   - Feature importance chart showing main environmental drivers.  
   - Interactive `Folium` map for exploring NDVI distribution.

---

## 📈 Results & Insights

### 🗺️ NDVI Map (2023)
- Dark blue areas represent **urban or barren zones** with low vegetation.  
- Yellow-green regions indicate **dense, healthy vegetation** (agriculture or forest).  
- The spatial gradient matches Amman’s real environmental conditions: greener in the north and west, drier in the south and east.

### ⚙️ Driver Importance
| Feature | Importance | Meaning |
|----------|-------------|---------|
| Elevation | ~0.57 | Strongest influence on NDVI — highlands support greener areas. |
| Rainfall | ~0.43 | Still important, but less dominant — suggests irrigation and topography play key roles. |

**Conclusion:**  
Vegetation health in Amman is influenced more by **elevation (topography)** than by rainfall alone, highlighting microclimatic effects in semi-arid regions.

---

## 🧰 Technologies Used
| Category | Tools / Libraries |
|-----------|-------------------|
| Remote Sensing | Google Earth Engine, geemap |
| GIS | rioxarray, rasterio, shapely, geopandas |
| Machine Learning | scikit-learn |
| Visualization | matplotlib, folium, seaborn |
| Environment | Jupyter Notebook (Python 3.13) |

---

## 🪶 How to Run Locally

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/<yourusername>/Geo_Environmental_Analysis.git
cd Geo_Environmental_Analysis
