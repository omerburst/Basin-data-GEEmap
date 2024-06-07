# Basin Data Code - Using GEE Account


## Introduction
This repository contains a Google Colab notebook designed to facilitate the analysis of drainage basins using geospatial data layers.

By leveraging the powerful geemap library, users can visualize and download various hydrological, topographical, and environmental datasets in GeoTIFF format.

The goal of this project is to provide an accessible tool for researchers, students, and environmental professionals to study drainage basins with ease.

A drainage basin, also known as a watershed or catchment area, is an area of land where all precipitation collects and drains off into a common outlet, such as a river, bay, or other body of water. 

Understanding drainage basins is crucial for managing water resources, predicting floods, and planning sustainable land use. 

They are fundamental units in hydrology and environmental science.

## Key Features

The Colab notebook includes a range of data layers that are essential for comprehensive drainage basin analysis:
  
* **River Order:** Displays the hierarchical classification of streams within the basin.
  
* **Land Cover:** Offers detailed maps of vegetation, urban areas, water bodies, and other land cover types.
  
* **Dams:** Highlights the locations of dams, which are critical for water management and flood control.
 
* **Groundwater Assessment:** Provides information on groundwater levels.
  
* **Topographic Indices:**

  * **Slope:** Measures the steepness or incline of the terrain, important for understanding erosion and runoff patterns.
  
  * **Height Above Nearest Drainage (HAND):** An index that measures the vertical distance between a point in the landscape and the nearest stream, useful for floodplain mapping.
  
  * **Topographic Wetness Index (TWI):** An index that helps to identify areas prone to saturation and potential runoff zones.
  
  * **Topographic Position Index (TPI):** Identifies the relative position of a location in the landscape, distinguishing between ridges, valleys, and flat areas.
  
  * **Compound Topographic Index (CTI):** Also known as the compound topographic wetness index, it combines slope and upstream contributing area to assess wetness potential.
  
  * **Stream Power Index (SPI):** Quantifies the erosive power of flowing water, based on slope and upstream catchment area.

  * **Sediment Transport Index (STI):** Estimates potential sediment transport capacity, combining slope and contributing area similar to SPI.

## How to Use the Notebook
**1) Visualization:** Users can interact with the map interface to explore different layers. Each layer can be toggled on or off to customize the view.

**2) Download:** Users can download selected layers as GeoTIFF files for further analysis in GIS software or other applications.
  
## Requirenments
The code is adapted to the Google Colab environment and requires an account in GEE (Google Earth Engine) in order to download the necessary data. A video explaining how to open an account in GEE can be found in the following link: https://www.youtube.com/watch?v=S0AzoP40cDI&t=8s

GEE website: https://earthengine.google.com/

## The Code

### A) Initializing the GEE account

In order to initialize your GEE account, you need to run the second cell in the code after you change to your own gee project name.

you can find your project name by entering to gee website, then press your profile - project info and under "Cloud Project:" you will find the name (Fig 1).

Fig 1.

<img width="955" alt="gee_project" src="https://github.com/omerburst/Basin-data-GEEmap/assets/95708635/75b407de-e980-4346-8683-8c40cc3f6206">


### B) Choosing the basin of interest

First, you need to choose your drainage basin. 

You can easily doing so by "draw a marker" button that appear in the geemap. Put the marker in the polygon of your watershed (Fig 2). 

Fig 2

<img width="491" alt="image" src="https://user-images.githubusercontent.com/95708635/224548590-6c263755-56e9-4fa2-be01-964c8f2d3ce4.png">


## Output

In the last cell you could download the layers to your own google drive folder. To do so, insert your desierd folder path, and basin name.

## References

Verkaik, J., Hughes J.D., Langevin, C.D., (2021). Parallel MODFLOW 6.2.1 prototype release 0.1 (6.2.1_0.1). Zenodo.

van Soesbergen, Arnout; Mulligan, Mark; Sáenz, Leonardo (2020): GOODD global dam dataset
figshare. Dataset. https://doi.org/10.6084/m9.figshare.9747686.v1

Donchyts, Gennadii, Hessel Winsemius, Jaap Schellekens, Tyler Erickson, Hongkai Gao, Hubert Savenije, and Nick van de Giesen. "Global 30m Height Above the Nearest Drainage (HAND)",
Geophysical Research Abstracts, Vol. 18, EGU2016-17445-3, 2016, EGU General Assembly (2016).

Amatulli, Giuseppe, Jaime Garcia Marquez, Tushar Sethi, Jens Kiesel, Afroditi Grigoropoulou, Maria M. Üblacker, Longzhu Q. Shen, and Sami Domisch.
"Hydrography90m: A new high-resolution global hydrographic dataset." Earth System Science Data 14, no. 10 (2022): 4525-4550.

Jaafar, H.H., Ahmad, F.A. & El Beyrouthy, N. GCN250, new global gridded curve numbers for hydrologic modeling and design.
Sci Data 6, 145 (2019). https://doi.org/10.1038/s41597-019-0155-x

Buchhorn, M. ; Lesiv, M. ; Tsendbazar, N. - E. ; Herold, M. ; Bertels, L. ; Smets, B. Copernicus Global Land Cover Layers-Collection 2. Remote Sensing 2020, 12Volume 108, 1044. doi:10.3390/rs12061044








