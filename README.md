# Examining Methods for Oil & Gas Infrastructure Detection in the Permian Basin

## Table of Contents  
- [Project Details](#project-details)  
- [Data Sources](#data-sources)  
- [Walk-Through](#walk-through)  
    1. [Interactive Mapping](#(1)-interactive-mapping)  
___

## Project Details

This is an exploratory project to investigate methods and available data sources to create an up-to-date repository of oil and gas infrastructure database. For the purposes of this study, we will be focusing on the Permian Basin, located in southwestern US between January 2020 to June 2021. Data sources will primarily be from remotely sensed imagery and satellite-based products indicative of O&G extraction activity. 

Active wellsites emit gas flares to burn off excess natural gas from crude oil and natural gas wells. However, approximately 11% of these towers can leak substantial quantities of methane and other gases due to some form of malfunction. Therefore, a top-down approach to (1) identify temporally consistent active wellsite locations, and to (2) quantify emissions is imperative in further understanding the impact of oil and gas production in the world.  

## Data Sources

A combination of high resolution imagery, and satellite-based products that detect methane emissions and gas flares were collected from January 2020 to June 2021. 

* 2018 NAIP (1m) Imagery
* Monthly Sentinel (10m) 
* Monthly TROPOMI - Methane Readings 
* VIIRS NOAA - Active Gas Flare Detections 


## Walk-Through

## (1) Interactive mapping

The initial part of this project is the exploratory visualization tool. It primarily relies of the Google Earth Engine API and ipywiget to customize user-based queries to visualize a subset of imagery and data layers at a monthly scale from Jan 2020 to June 2021 within the Permian Basin. 

The green points indicate VIIRS (375m) active fire hotspots, representing the detection of gas flares during the time period. The red point are the centroid of unique individual clusters, indicative of active flaring sites. 

The clusters were defined using the DBSCAN (Density-Based Spatial Clustering of Applications with Noise) algorithm with minimum sample size of 5. The yellow points are the outliers that did not fit into a unique cluster class.    

<img src="docs/Tab1_VisLayers.png" alt="Tab1_VisLayer">
Figure 1. Interactive mapping application to select data layer visualization by month. Specify map center and zoom for additional control. 


<img src="docs/Tab1_VisLayers2.png" alt="Tab1_VisLayer2">
Figure 2. Zoomed out to the entire extent of the basin for May 2021. Methane quantity via TROPOMI can be seen to coincide with active flare site hotspots. 