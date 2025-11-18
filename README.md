# Mapping the rooftop solar potential of UBC

## Preamble

### Motivation

Today we'll be learning about mapping renewable energy by looking for rooftops suitable for solar panel installation in an urban area of Vancouver. We'll be looking at the Fairview neighbourhood, located just south of False Creek. This neighbourhood provides an excellent backdrop for our experiment with solar potential mapping, it has a mix of zoning including commercial, residential, high, and low density urban areas. This gives us plenty of different types of rooftops to look at.

### How this exercise will work

While we're running our demo (not the actual presentation), feel free to wave down any of the presenters who are not actively presenting to ask questions or get help setting up your environment. We only have so much time to run this exercise, so we won't pause until the end (unless Arc is taking its time to process data 💤).

This exercise has a lot of data processing! That means we might not get through all of it in our alotted presentation time. That's okay though! All the material we've presented will stay available in this repository for quite some time (if not forever). We'll choose a natural breaking point and you can continue the exercise on your own time if you'd like :)

### The Dataset

The data for this lab has been acquired from the [City of Vancouver's open data portal](https://opendata.vancouver.ca/). We've pre-processed the data to minimize the amount that needs to be downloaded and worked on. Here's a quick summary of what we've done:

- We extracted the Fairview polygon from the [local area boundaries](https://opendata.vancouver.ca/explore/dataset/local-area-boundary/information/?disjunctive.name) dataset. This was used to clip other datasets to our area of interest.
- LAS data was downloaded from the [LiDAR 2022](https://opendata.vancouver.ca/explore/dataset/lidar-2022/information/) dataset within the Fairview extent. These files were used to create a LiDAR dataset in ArcGIS, which was then converted into a DEM spanning the dataset. Finally, the DEM was clipped to the Fairview boundaries.
- The latest [Building Footprints](https://opendata.vancouver.ca/explore/dataset/building-footprints-2015/information/) (from 2015) has been clipped to the Fairview extent. No additional processing was required.

> [!NOTE]
> Please download the provided datasets to your machine **before** we get to the exercise portion of our presentation! You can find the dataset here.

## The Exercise

### 1. Setting up your environment

Load data into Arc. Create a hillshade?

### 2. Calculating solar radiation

How to do it

A brief comment: what is solar radiation? Irradiance? Why so many words!

### 3. Eliminating non-suitable rooftops

Calculating our layers for suitability -> slope, aspect, output
- Caveat: Our LiDAR kinda sucks

Elimination criteria -> 
https://natural-resources.canada.ca/sites/nrcan/files/canmetenergy/files/pubs/SolarReadyGuidelines_en.pdf

1. Slope must be less than 60 degrees.
2. We don't want the roof facing north.
3. Any area with under 800 

### 4. Calculating zonal statistics

Here are the steps you got to follow:

Mask with buildings and use our filtered power potential
Join it back into the building footprints

### 5. Output our final selection of rooftops

7. Make a selection to select all the buildings w/ a certain total area of usable rooftop

## Acknowledgements

