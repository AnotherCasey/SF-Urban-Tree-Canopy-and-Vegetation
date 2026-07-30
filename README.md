# Urban Tree Canopy and Vegetation Mapping

*A reproducible remote sensing workflow for estimating urban tree canopy and total vegetated land cover in San Francisco using Google Earth Engine, NAIP aerial imagery, Sentinel-2 satellite imagery, and LiDAR.*

![Project Status](https://img.shields.io/badge/status-active-brightgreen)
![Platform](https://img.shields.io/badge/platform-Google%20Earth%20Engine-blue)
![Language](https://img.shields.io/badge/language-JavaScript-yellow)
![GIS](https://img.shields.io/badge/GIS-ArcGIS%20Pro-green)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

---

## Overview

Urban vegetation provides numerous ecosystem services including carbon sequestration, stormwater interception, urban heat mitigation, wildlife habitat, and improvements to human health. Reliable estimates of vegetation and tree canopy are essential for monitoring change over time and supporting evidence-based urban planning.

This repository contains reproducible workflows developed to estimate:

- 🌳 Urban Tree Canopy (UTC)
- 🌿 Total Vegetated Land Cover

for the **City and County of San Francisco** using publicly available remote sensing datasets and cloud-based geospatial analysis.

The project integrates multiple remote sensing products to generate GIS-ready raster outputs and area estimates that can be updated as new imagery becomes available.

---

## Objectives

- Develop a reproducible workflow for estimating total vegetation cover.
- Estimate urban tree canopy using spectral and LiDAR-derived height information.
- Produce GIS-ready raster products for visualization and further analysis.
- Demonstrate an automated workflow that can be rerun as new imagery becomes available.

---

## Results

| Product | Estimate |
|----------|----------:|
| Urban Tree Canopy | **5,276 acres (17.5%)** |
| Total Vegetation (NAIP) | **7,602 acres (25.2%)** |
| Total Vegetation (Sentinel-2) | **9,575 acres** |

---

## Technical Highlights

- Google Earth Engine
- Remote sensing
- Sentinel-2 multispectral imagery
- USDA NAIP aerial imagery
- LiDAR canopy height models
- NDVI analysis
- ArcGIS Pro
- GIS raster processing
- Automated geospatial workflows
- Reproducible scientific analysis

---

## Workflow Summary

### Total Vegetation

1. Acquire NAIP or Sentinel-2 imagery
2. Calculate NDVI
3. Mask clouds (Sentinel-2)
4. Remove building footprints
5. Apply NDVI threshold
6. Calculate vegetated area
7. Export GIS-ready raster products

### Urban Tree Canopy

1. Calculate vegetation using NDVI
2. Import LiDAR Height Above Ground raster
3. Classify vegetation taller than 8 feet
4. Generate Urban Tree Canopy raster
5. Calculate canopy area
6. Export raster and summary statistics

---

## Repository Structure

```text
SF-Urban-Tree-Canopy/
│
├── README.md
├── LICENSE
│
├── docs/
│   ├── methodology.md
│   ├── workflow.md
│   └── metadata.md
│
├── figures/
│
├── scripts/
│   ├── gee/
│   ├── exploratory/
│   ├── python/
│   └── r/
│
├── outputs/
│
└── data/
```

---

## Data Sources

### Remote Sensing

- Sentinel-2 Harmonized Surface Reflectance
- USDA National Agriculture Imagery Program (NAIP)
- USGS LiDAR-derived Height Above Ground raster

### Vector Data

- City and County of San Francisco boundary
- San Francisco building footprints

---

## Outputs

The workflow produces:

- Urban Tree Canopy raster
- Total Vegetation raster
- Cloud-Optimized GeoTIFF (COG)
- GIS-ready shapefiles
- Vegetation area estimates
- Tree canopy area estimates

---

## Reproducibility

The workflows are designed to be rerun using updated imagery with minimal modification.

Most processing is performed in **Google Earth Engine**, allowing analyses to be reproduced without downloading large remote sensing datasets.

Output rasters can be exported directly to ArcGIS Pro or other GIS software for visualization and further analysis.

---

## Future Improvements

- Multi-year vegetation change detection
- Time series analysis
- Automated annual updates
- Additional accuracy assessment
- Species-specific vegetation classification
- Integration with additional remote sensing products

---

## License

This repository is released under the MIT License.

---
