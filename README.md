# Environmental-Data-Analysis
This repository details analysis on land cover types, precipitation, and vegetation index.Data used in the data preprocessing stage included land cover, precipitation, NDVI imagery, and IN polygon shapefile.
Vegetation index, precipitation, and land cover types are essential concepts in environmental science and remote sensing, providing valuable insights into ecosystem health, climate dynamics, and land use patterns. Understanding the interplay between these factors is crucial for monitoring environmental changes, assessing ecosystem resilience, and informing sustainable land management practices.

# Data Information
Data Information can be publicly assessed below.
Please check the table for information about the three datasets.

MOD13A1: https://lpdaac.usgs.gov/products/mod13a1v006/Links to an external site.

MCD12Q1: https://yceo.yale.edu/modis-land-cover-product-mcd12q1Links to an external site.

TMPA/3B43 Rainfall Estimate:  https://disc.gsfc.nasa.gov/datasets/TRMM_3B43_7/summary

# Project Requirement
All the datasets are processed to match their coordination systems. The cleaned datasets have the same coordination systems as the land cover/land use (MCD12Q1) data. 
Transfer the projection of the IN polygon to match the projection of the land cover images.
Transfer the projection of the precipitation data to match the projection of the land cover images.
Mask NDVI, land covers, and precipitation data over the IN region.
Merge 16-day NDVI data into monthly data.
Transfer NDVI data and land cover to data frames. Each pixel is 500m * 500m. When transferring the pixels to data frames, the center of a pixel will have a point.
Despite the different spatial resolutions of NDVI (Land cover) and precipitation data, we didn’t downscale the precipitation data from 0.25 degrees to 500m. We directly used the points (x and y coordinates) to extract the upscaled precipitation data. Thus, the scale of precipitation is much larger and coarser than that of the NDVI and land cover data.

You are required to conduct the data analysis and data visualization for the final project:
1. Spatial mapping NDVI and land cover/land use in 2019 (Refer to Module 4 and the review video of Modules 3-5)
   
- You can map the average NDVI in 2019 or a specific date NDVI in 2019.
- Describe the spatial  distributions of NDVI and land cover/land use

2. ANOVA analysis of NDVI with month and land cover types using data in 2019 (Refer to Modules 5 and 6)

- Two-way ANOVA (one dependent variable and two independent variables)
- Interpret the ANOVA analysis
  
3. Ordinary linear regression analysis of NDVI with precipitation  (Refer to Modules 5 and 6)

- Please remove the missing value if there is any.
- Interpret the linear regression result
  
4. Time series analysis with NDVI time series from 2013-2022 over croplands (Refer to Modules 7 and 8)

- Plot and decompose time series of NDVI
- Split the data into two parts: training data: 2013-2020; test data: 2021-2022
- Model the time series analysis and forecasting with the training data and valid it with the test data
- Interpret your time series analysis
