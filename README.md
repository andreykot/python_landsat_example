### Using Python with satellite images

You are given 6 raster files. All rasters have the same bounding box but are the annual composite (Landsat 8, 30 m resolution) of different years from 2015 to 2020. Each file has 7 bands that are associated with ["B2", "B3", "B4", "B5", "B6", "B7", "pixel_qa"] described [here](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T1_SR) respectively (Collection 1).

1.	You are given an AOI shapefile. Use this shapefile to clip each individual raster file and write down the new rasters. From now, only use the clipped rasters.

2.	Read the clipped raster file for 2020. Only choose the RGB bands, plot a true-colour image, and save it to another raster file called 2020_true_color_clipped.tif (It should only include 3 bands).

3.	Calculate the average NDVI of all pixels for each year (each clipped raster) and look at the time series of this variable (your code should produce a time series plot + CSV file containing the NDVI numbers).

4.	Write some code to save the CSV file that you created in the previous step in an AWS S3 bucket in the cloud (since you don't have access to a real S3 bucket, this is hypothetical exercise).

5.	When working with a time series of raster files, it is more convenient to use only one raster file where each band is associated with one data point in time. Only considering the RED CHANNEL of each clipped raster, write some code that produces a raster file with 6 bands where each band is the values of RED CHANNEL for each year (2015 to 2020). 

6. Calculate the total area of the clipped raster (from the previous section), Note that when calculating the area of a raster, you need to make sure the raster is in the right projection to mitigate any projection error.
