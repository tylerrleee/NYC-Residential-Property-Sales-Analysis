# NYC Residential Property Sales Analysis


A reproducible R pipeline for ingesting, cleaning, geocoding, and visualizing five-borough rolling-sales data from the NYC Department of Finance (May 2024–Apr 2025), with spatial analysis via the PLUTO shapefile.
Processed & Cleaned Large-Scale Sales Data: Ingested and standardized over 120,000 rolling‑sales records spanning May 2024–April 2025 across all five NYC boroughs, recoding 30+ variables and handling 25,000+ zero‑price deed transfers to ensure a clean, analysis‑ready dataset.


---

## 📋 Table of Contents

1. [Project Overview](#project-overview)  
2. [Data Sources](#data-sources)  
3. [Features](#features)  
4. [Installation & Setup](#installation--setup)  
5. [Usage](#usage)  
6. [Methodology](#methodology)  
7. [Key Visualizations](#key-visualizations)  
8. [Results & Insights](#results--insights)  
9. [Contributing](#contributing)  
10. [License](#license)  
11. [Contact](#contact)  

---
## Project Overview

- **Goal:** Examine how transaction volume, price, and building class distributions vary across NYC’s five boroughs.  
- **Timeframe:** May 2024 – April 2025  
- **Scope:**  
  - 120,000+ sales records  
  - All residential building classes (1-Family through Walk-up Condos)  
  - Spatial centroid join using PLUTO shapefile  

Geocoded 100% of Transactions: Merged Department of Finance sales data with the PLUTO shapefile (856,734 features) to compute centroids and attach latitude/longitude to every record, enabling precise spatial mapping of property sales.
---

## Visualizations

![Average Sale Price in each Borough]([http://url/to/img.png](https://github.com/tylerrleee/NYCsales/blob/LAB5/visualizations/avgsalepriceperborough.pdf))

![Property Sale Density of NYC]([http://url/to/img.png](https://github.com/tylerrleee/NYCsales/blob/LAB5/visualizations/densitypropertysale.pdf))

![Property Sales in NYC]([http://url/to/img.png](https://github.com/tylerrleee/NYCsales/blob/LAB5/visualizations/propertysales%20innyc.pdf))

![Proportions of Building Type purchased]([http://url/to/img.png](https://github.com/tylerrleee/NYCsales/blob/LAB5/visualizations/proportionsofsales.png))


## Data Sources

1. **NYC Rolling Sales** (Dept. of Finance CSVs)  
2. **PLUTO Shapefile** (NYC Planning)  
3. **Derived Summaries** (average price per borough, density maps, etc.)  

All raw data and intermediate files live in the `data/` folder.

---

## Features

- **ETL pipeline in R** using `dplyr`, `sf`, `lubridate`, `stringr`  
- **Automated geocoding**: centroids of 856,734 PLUTO polygons → lat/long  
- **Reproducible plots** with `ggplot2` + `patchwork`  
- **Interactive map** export via `leaflet` (optional)  
- **Report generation** in R Markdown  

---

