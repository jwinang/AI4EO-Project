# AI4EO-Project
Video link：替换

---

# 💧 Detection of Inland Water Bodies Using Machine Learning

## 📑 Table of Contents

* [About The Project](#about-the-project)
* [Background](#background)
* [The SENTINEL-2 Satellite](#the-sentinel-2-satellite)
* [Machine Learning Methodology: K-Means Clustering](#machine-learning-methodology-k-means-clustering)
* [Problem Statement](#problem-statement)
* [Environmental Cost Assessment](#environmental-cost-assessment)
* [Datasets Used](#datasets-used)
* [Results](#results)
* [References](#references)

---

## 📌 About The Project

This project investigates the use of unsupervised machine learning — specifically **K-means clustering** — to classify **inland water bodies** in satellite imagery obtained from **SENTINEL-2**. Two regions with vastly different water characteristics are examined: **Selin Co** in the Tibetan Plateau, and the **Finnish Lakeland**. The goal is to evaluate whether machine learning can enhance or outperform traditional remote sensing indices such as the **NDWI (Normalized Difference Water Index)** in complex hydrological conditions.

---

## 🌍 Background

Inland water bodies — lakes, rivers, wetlands, and reservoirs — are vital to ecosystems, agriculture, human settlement, and climate regulation. However, they are increasingly vulnerable to **climate change** and **human impacts**, making accurate, efficient monitoring of their extent and change over time crucial.

**Remote sensing** using satellites like SENTINEL-2 provides a scalable, low-cost solution. This project explores whether unsupervised learning techniques can augment or surpass traditional spectral indices in identifying water features, especially in areas with **sediment-laden water**, **seasonal variability**, or **fragmented landscapes**.

---

## 🛰️ The SENTINEL-2 Satellite

The **SENTINEL-2** mission is part of the European Space Agency’s **Copernicus Programme**, designed to monitor Earth’s land surface in high detail. Key characteristics include:

* **13 multispectral bands** ranging from visible to shortwave infrared
* **Spatial resolutions** of 10m, 20m, and 60m depending on the band
* **High revisit frequency**, allowing for timely monitoring of water dynamics

These features make SENTINEL-2 ideal for inland water monitoring across diverse environments.

---

## 🤖 Machine Learning Methodology: K-Means Clustering

K-means clustering is an **unsupervised learning algorithm** that partitions data into *k* distinct clusters based on feature similarity. In this project:

* K-means is applied on **selected spectral bands** from Sentinel-2
* Results are compared against the **NDWI baseline**
* The approach does not rely on labeled training data, making it suitable for scalable, exploratory analysis

We test two band combinations:

1. Bands **B03 (Green)** and **B08 (NIR)** — used to compute NDWI
2. Bands **B05 (Red Edge)** and **B11 (SWIR)** — used in the **Sentinel Water Index (SWI)** proposed by Jiang et al., 2020

---

## 🧠 Problem Statement

Inland water bodies play a critical role in global ecology and climate. Comprising lakes, reservoirs, rivers, and ephemeral water bodies, they support biodiversity, human economies, agriculture, and hydrological cycles. However, due to **climate change**, **urbanisation**, and **pollution**, many of these water bodies are changing in unpredictable ways, some even disappearing.

Timely, accurate monitoring is thus essential. Traditional field methods are **costly, time-consuming, and labor-intensive**. In contrast, **satellite-based remote sensing** is **global, frequent, and cost-effective**.

The **Normalized Difference Water Index (NDWI)** is a widely used spectral method for identifying water, but it has limitations — particularly in **sediment-rich**, **urban**, or **mixed land-cover** environments. This project explores whether **unsupervised machine learning**, using K-means clustering on Sentinel-2 imagery, can overcome these limitations.

---

## 🌱 Environmental Cost Assessment

To assess the **environmental footprint** of this project, we consider the following:

* ✅ **Data Source**: Sentinel-2 imagery is publicly available and collected by satellites already in orbit. No new launches or field surveys were needed, making data acquisition essentially **carbon-neutral**.
* ✅ **Computation**: The project was run on **Google Colab**, which utilizes Google Cloud infrastructure. According to Google, their data centers have been **carbon neutral since 2007**, and are now operating with **100% renewable energy matching**.
* ✅ **Storage & Sharing**: Datasets were downloaded only as needed, and no redundant storage or duplication was performed.

📉 **Estimated Carbon Impact**: Minimal, primarily limited to personal electricity use during development. All methods were designed to be **computationally lightweight**, avoiding GPU-intensive training or excessive storage.

Overall, this project represents a **low-environmental-cost approach** to high-impact geospatial research.

---

## 📦 Datasets Used

This project uses **Sentinel-2 L2A** surface reflectance imagery, which has undergone atmospheric correction. Two distinct geographic regions were selected to test the robustness of unsupervised classification methods for inland water detection:

* **Selin Lake, Tibet** – A large inland lake located on the Tibetan Plateau. The region’s high elevation, minimal vegetation, and varying seasonal water levels provide a challenging environment for water body detection using spectral data alone.
* **Finland Lake District** – One of the largest lake districts in Europe, characterized by a dense distribution of small and medium-sized lakes interspersed with forested land. The fragmented nature of the landscape makes it a useful test case for evaluating the ability of machine learning algorithms to accurately distinguish between land and water on a fine scale.

These areas were chosen due to their contrasting hydrological and spectral characteristics, allowing for a comprehensive evaluation of both traditional and ML-based classification techniques.

---

## 📥 Downloading Datasets

The original Sentinel-2 datasets are **not included** in this repository. However, you can download the same data from the **[Copernicus Dataspace Browser](https://dataspace.copernicus.eu/)**. A free account is required to access the files.

To obtain the datasets:

1. Navigate to the [Copernicus Dataspace Browser](https://dataspace.copernicus.eu/).
2. Go to the **Search** tab.
3. Enter the following filenames in the search bar to locate the scenes:

* `S2A_MSIL2A_20250528T045241_N0511_R076_T45SXR_20250528T080601.SAFE` – Selin Lake (Tibet)
* `S2C_MSIL1C_20250526T095051_N0511_R079_T35VNJ_20250526T132942.SAFE` – Finland Lake District

4. Download and unzip the `.SAFE` folders in your local or cloud-based workspace.

> 💡 Tip: If you're working on Google Colab, upload these files to your Google Drive and mount the drive in your notebook.


---

## 📊 Results

* **NDWI vs K-Means**: In both regions, K-means matched or exceeded NDWI performance, especially in **fragmented** or **sediment-rich** conditions.
* **Visual Evaluation**: K-means was better at discriminating complex boundaries in small lakes (Finnish Lakeland) and sediment-rich rivers (Selin Co).
* **Limitations**: Without ground truth labels, evaluation relies on qualitative analysis and NDWI comparison.

---

## 👩‍💻 Author

This project was developed as part of the final assignment for the AI4EO at UCL.

