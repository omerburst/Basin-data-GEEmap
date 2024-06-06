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
 
* **Groundwater Assessment:** Provides information on groundwater levels, quality, and recharge areas.
  
* **Topographic Indices:**

  * **Slope:** Measures the steepness or incline of the terrain, important for understanding erosion and runoff patterns.
  
  * **Height Above Nearest Drainage (HAND):** An index that measures the vertical distance between a point in the landscape and the nearest stream, useful for floodplain mapping.
  
  * **Topographic Wetness Index (TWI):** An index that helps to identify areas prone to saturation and potential runoff zones.
  
  * **Topographic Position Index (TPI):** Identifies the relative position of a location in the landscape, distinguishing between ridges, valleys, and flat areas.
  
  * **Compound Topographic Index (CTI):** Also known as the compound topographic wetness index, it combines slope and upstream contributing area to assess wetness potential.
  
  * **Stream Power Index (SPI):** Quantifies the erosive power of flowing water, based on slope and upstream catchment area.

  * **Sediment Transport Index (STI):** Estimates potential sediment transport capacity, combining slope and contributing area similar to SPI.

## How to Use the Notebook
Visualization: Users can interact with the map interface to explore different layers. Each layer can be toggled on or off to customize the view.
Download: Users can download selected layers as GeoTIFF files for further analysis in GIS software or other applications
  
## Requirenments
The code is adapted to the Google Colab environment and requires an account in GEE (Google Earth Engine) in order to download the necessary data. A video explaining how to open an account in GEE can be found in the following link: https://www.youtube.com/watch?v=S0AzoP40cDI&t=8s

GEE website: https://earthengine.google.com/

## 3) The Code

### A) Initializing the GEE account

In order to initialize your GEE account, you need to run this cell of the code. Click the link that appears on your screen (Fig 1). After following the instructions and generating a token, you will receive a verification code. Copy and paste the code to the box that reads: " Enter verification code:" and then press Enter (Fig 1).

<img width="602" alt="image" src="https://user-images.githubusercontent.com/95708635/224546720-7338423a-db5d-4abb-8f85-4d86e2ebe7bb.png">

Fig 1.

### B) Choosing the river of interest

To run SatVITS-Flood, you need to insert the coordinates of the pixel that represents the river of interest. There are two options for that: 
**option 1:** If you know the coordinates, insert them directly where it says "option 1" (Fig 2)

<img width="310" alt="image" src="https://user-images.githubusercontent.com/95708635/224547312-95df9614-9ed3-4448-ba14-92e5a5d77ac2.png">

Fig 2.

**Option 2:** Using the map.
If you are not sure of the coordinates, you can first display the precipitation layer to see the hyper-arid regions (yellow regions in Fig 3.A). The NDVI STD (Standart Deviation) around your river can be also displayed. This NDVI STD layer can help you select the pixel of interest (near the river). Notice that greener pixels mean high changes in vegetation, which might be an indication of flood effect (Fig 3.B; see further explanation in Burstein et al., 2023 article: https://agupubs.onlinelibrary.wiley.com/doi/epdf/10.1029/2023WR035164). Once you decided which is the pixel that represents your river, use the "draw a marker" option to get its coordinates (Fig 3.B).

<img width="491" alt="image" src="https://user-images.githubusercontent.com/95708635/224548590-6c263755-56e9-4fa2-be01-964c8f2d3ce4.png">

Fig 3

In both options, you can add your river_name to save the name on your output CSV file. You can also change the month of the start of the hydrological year (Fig 2). 

After inserting the coordinates of the hyper-arid river, run the code and get the flood detection year, as well as the flood magnitude (volume and duration), from SatVITS-Flood.

## 4) Output

The app will automaticaly download a CSV file to your computer. This CSV file will contain information about the year of the flood, its volume and duration (Fig 4). When SatVITS-Flood is unable to estimate the flood's volume or duration, the year of the flood will be the only data displayed.

<img width="452" alt="image" src="https://user-images.githubusercontent.com/95708635/224549415-cedc8abb-1436-4bc7-8b9d-96b3dd2cb246.png">

Fig 4

## 5) Supplements

We add our raw code used to develop this app. The user can use these codes directly to run SatVITS-Flood on his own data.

Links to the code in GEE for downloading the VIs time series:

MODIS: https://code.earthengine.google.com/3061df7bf284f085233d9a5172d25292

Landsat: https://code.earthengine.google.com/8577a70078a5c0d648274ebb551d2f26

AVHRR: https://code.earthengine.google.com/7aaa10e7a7f40fb8e97747fdbb2157fd
