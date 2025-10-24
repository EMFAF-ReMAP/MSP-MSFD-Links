# 🧭 MSP & MSFD Links  
**Connecting Maritime Spatial Planning with Marine Strategy Framework Directive assessments**

---

## 📘 Overview
**MSP & MSFD Links** is a tool developed within the **ReMAP project**. Its primary objective is to **connect the spatial planned uses of the sea from Maritime Spatial Plans (MSPs)** with the **assessment data produced under the Marine Strategy Framework Directive (MSFD)**.  

The tool supports:
- MSP planners in the **planning, review, and update** of spatial plans  
- MSFD officers in exploring **spatial overlaps and status of uses in Marine Reporting Units (MRUs)**  
- Users in linking MSP spatial allocations with Good Environmental Status (GES) indicators

---

![image](https://github.com/user-attachments/assets/c690a4ea-e6ac-43d9-9e7c-6ba74a5fbe95)


## 🌍 Data Sources
The tool integrates the following authoritative European datasets:
- **MSP Zoning Elements** via [EMODnet Human Activities](https://emodnet.ec.europa.eu/en/human-activities)  
- **MSFD assessment data** via [WISE Marine](https://water.europa.eu/) (2018) and Repornet (2024)  

Additionally, the Italian and French Mediterranean MSPs have been harmonized according to the EMODnet MSP data model. All input data are **cleaned for topological consistency** and stored in **Parquet format** for optimized performance.

---

## 🧩 Architecture
MSP & MSFD Links is implemented as an **interactive web application** using **[Streamlit](https://streamlit.io/)**. It follows a **modular architecture** separating:
- Data preprocessing  
- Analysis (spatial overlays and assessment linkages)  
- Visualization (interactive charts, maps, and tables)  

The tool is **containerized** (Docker-ready) for reproducible deployment.

---

## ⚙️ Technology Stack

| Component | Description |
|------------|-------------|
| **Python** | Core programming language |
| **Streamlit** | Framework for interactive web applications |
| **pandas / geopandas** | Tabular and geospatial data handling |
| **shapely** | Geometry validation and topology correction |
| **folium** | Interactive map visualization (Leaflet.js) |
| **plotly, matplotlib, seaborn** | Interactive and static charts |
| **rasterstats** | Linking raster and vector data |
| **pyarrow, fastparquet** | Efficient I/O with Parquet files |

---

## 📥 Input Data
- **MSP spatial plans** (Zoning Elements) via EMODnet, including harmonized Italian and French Mediterranean plans  
- **MSFD assessment data**:
  - 2018 assessment from WISE Marine  
  - 2024 assessment from Repornet (partial coverage: Estonia, Germany, Spain)  

Input data are preprocessed to ensure **topological consistency** (self-intersections, overlaps, invalid geometries removed) and stored in Parquet for interactive use.

---

## 📊 Analyses and Outputs
MSP & MSFD Links allows users to perform **spatial overlay analyses** connecting MSP spatial uses with MSFD assessment results. Outputs include:

- **Sankey diagrams** – showing contributions of MSP uses to GES assessment  
- **Treemaps** – hierarchical view of MSs, GES components, and assessment features  
- **Interactive maps** – display GES status and spatial coherence for selected areas  
- **Downloadable data** – GeoJSON for GIS analysis, CSV for tabular results  

Users can select:
- **MSFD reporting period** (2018 or 2024)  
- **Spatial scale** (country, transboundary area, or project profile: Baltic, NW Mediterranean, Galicia)  
- **Sea uses** and **functions** from MSPs  
- **MSFD assessment level**: Overall, Element, Criteria, or Parameter  

Analysis outputs include interactive charts, maps, and tables, with **full-screen and download options**, and use the **same color conventions as WISE Marine dashboards**.

---

## 🚀 Deployment & Access
- **Online version (v0.11.0):**  
  🔗 [https://geoapps.tools4msp.eu/ReMAP_MSP_MSFD](https://geoapps.tools4msp.eu/ReMAP_MSP_MSFD)

- **Source code:**  
  🔗 [https://github.com/EMFAF-ReMAP/MSP-MSFD-Links](https://github.com/EMFAF-ReMAP/MSP-MSFD-Links)

---

