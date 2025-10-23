# Banana Tree Detection using Template Matching and Geospatial Analysis

This repository contains a Jupyter Notebook detailing a geospatial project focused on detecting and mapping banana trees within a specified area. The methodology combines remote sensing image processing with a template matching algorithm to identify potential tree locations.

<img width="664" height="530" alt="results_banana_trees" src="https://github.com/user-attachments/assets/5fda75aa-c901-4ada-9cab-1a8f393d05f6" />

## 🚀 Features

- **Geospatial Data Handling**: Utilizes `rasterio` and `geopandas` for reading, analyzing, and plotting high-resolution raster imagery and vector point data.  
  - Works with a raster image: `Rst/Banana.tif` (4 bands: Red, Green, Blue, Alpha)  
  - Uses a point shapefile: `Shp/points.shp` for reference or validation  

- **Template Matching**: Implements the `skimage.feature.match_template` function to search for a predefined banana tree canopy template (`Template/banana.png`) within the larger raster image.

- **Detection Filtering**: Uses a clustering-based approach (`birchAlgorithm`) to refine template matching results, consolidating detections and reducing false positives.

- **Visualization**: Displays detected point locations overlaid on the source raster data using `matplotlib`.

- **Output**: Final detected banana tree locations are saved to a CSV file for further analysis.

## 🛠️ Requirements

The core functionality is implemented in the provided Jupyter Notebook: `banana tree detection 01.ipynb`.

### Python Libraries
To run the notebook, ensure you have the following libraries installed:

- `matplotlib`
- `geopandas`
- `rasterio`
- `scikit-image`
- `numpy`
- `Pillow`


```bash
pip install matplotlib geopandas rasterio scikit-image numpy Pillow
