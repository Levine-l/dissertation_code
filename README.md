# Dissertation Code

This repository contains the analysis code supporting the dissertation:

**Evaluating the Added Value of Sentinel-1 SAR for Crop Type Classification in East Anglia Using CROME and Sentinel Time Series Data**

The study compares a Sentinel-2 optical Random Forest baseline with a combined Sentinel-1 and Sentinel-2 model for eight crop classes. Model results are interpreted as agreement with CROME 2022 holdout labels. UKCEH Land Cover plus: Crops 2022 is used as a secondary benchmark.

## Workflow

| Folder | Purpose |
| --- | --- |
| `0_preprocessing` | Study-area preparation, CROME class harmonisation and data inspection |
| `1_sentinel_2_baseline` | Sentinel-2 optical baseline |
| `2_sentinel1_sentinel2_model` | Paired Sentinel-2 and Sentinel-1 plus Sentinel-2 comparison |
| `3_spatial_error_analysis` | Class, county and disagreement analysis at the point level |
| `4_ukceh_benchmark_comparison` | Comparison with the UKCEH crop map benchmark |
| `5_rf_sensitivity_check` | Random Forest robustness checks |
| `6_crop_profile_geography` | Crop profile clustering and SAR comparison at the zone level |

The numbered folders follow the main order of the analysis.

## Running the notebooks

The notebooks were developed locally and in Google Colab, so root paths may be slight differences between codes. The data intensive stages were run primarily in Colab because the data were stored in Google Drive.

The Earth Engine require authentication and access to an Earth Engine project.

Main Python packages include:

`earthengine-api`, `geemap`, `geopandas`, `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `folium`, `libpysal` and `esda`.

## Data

Original source datasets are not distributed in this repository. They are:

- CROME 2022
- UKCEH Land Cover plus: Crops 2022
- Sentinel-1 and Sentinel-2 imagery
- ONS administrative boundaries

Selected derived tables and figures are included to document the dissertation results. 

## Visualisation

Interactive maps and GEE app are available at:

https://github.com/Levine-l/crop_map
https://levine-l.github.io/crop_map/
