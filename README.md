# AI4EO-Project
Video link：替换

# Land Cover and Land Use Classification Using Sentinel-2 Imagery and IRIS

## 🌍 Project Overview

This project focuses on classifying various land cover and land use types using Sentinel-2 satellite imagery, including water bodies, vegetation, urban areas, and bare land. We utilize the **IRIS** annotation tool for manual labeling and apply both supervised and unsupervised machine learning techniques for classification tasks.

Our goal is to demonstrate the effectiveness of IRIS in generating training masks and compare classification accuracy against traditional machine learning methods.

---

## 📌 Objectives

- Acquire Sentinel-2 imagery using Google Earth Engine (GEE) or Copernicus Dataspace.
- Annotate land cover categories using the IRIS framework.
- Train and evaluate classification models (Random Forest, KMeans, etc.).
- Compare performance of IRIS labeling vs unsupervised methods.
- Assess the environmental cost of model training using energy tracking tools.

---

## 🛰️ Data Source

- **Satellite**: Sentinel-2 MSI (Multispectral Instrument)
- **Bands Used**: B2 (Blue), B3 (Green), B4 (Red), B8 (NIR)
- **Data Access**: 
  - Google Earth Engine ([https://code.earthengine.google.com/](https://code.earthengine.google.com/))
  - Copernicus Dataspace Ecosystem ([https://dataspace.copernicus.eu/](https://dataspace.copernicus.eu/))

---

## 🧪 Methodology

1. **Image Ingestion & Preprocessing**  
   - Selection of AOI (Area of Interest) and date range  
   - Image normalization, band stacking

2. **Manual Annotation (IRIS)**  
   - Use IRIS to generate labeled training masks (e.g. water, vegetation, urban)

3. **Classification Models**  
   - Supervised: Random Forest using IRIS-labeled masks  
   - Unsupervised: KMeans clustering on spectral bands

4. **Evaluation Metrics**  
   - Confusion matrix, IOU (Intersection over Union), pixel-wise accuracy

5. **Environmental Impact**  
   - CodeCarbon to estimate model energy consumption and carbon emissions

---

## 📁 Project Structure





## 👩‍💻 Author

This project was developed as part of the final assignment for the AI4EO at UCL.

