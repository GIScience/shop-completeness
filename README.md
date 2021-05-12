# Assessing shop completeness in OpenStreetMap

These codes estimate the completeness of OSM retail stores of two states in Germany, Baden-Württemberg and Saxony, via an intrinsic approach using the data history and investigate how the urban-rural gradient and socio-economic factors (gross domestic product, unemployment rate and proportion of academics) were associated with the estimated completeness of OSM retail stores.

Installation
The code was created in R version 3.6.1. and use the packages sf, RCurl, geojsonio, tidyverse, ggplot2, httr, readtext, readr, rapiclient, sf, geojson, geojsonsf, geojsonR, tmap, tmaptools, rgdal, osmdata, rnaturalearth, lubridate, stats, nlstools, dplyr, MASS, VGAM, polycor, plotly, car, ggeffects and ggpubr.
The inputs for each codes are available under the file "Data".




## Documentation
The analysis consists of three consecutive codes. 
1. Data query of OSM retail stores via the ohsome API at https://api.ohsome.org 
The code in getData_OSMretail.Rmd creates a table retailData.csv including the data history of OSM retail stores per month and at district level from 01/2018 until 01/2020, that is used as input for the second code.
2. Non-linear Regression of the data history (nls_OSMretail.Rmd)
The code creates a table nlsData.csv including the criteria for selecting the best fit and further information of the non-linear regression by varied limited growth functions. 
The table, that contains the estimated completeness level and the selected fit function as well as the plots of the selected fits for the completeness estimation are available under “results”.
3. Investigate the influence of factors on the estimated completeness level. (GLM OSMretail completeness.Rmd)
