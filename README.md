# Mapping the rooftop solar potential of UBC

So you want to map solar potential? Well you're going to have to grab a couple files first.


https://abacus.library.ubc.ca/file.xhtml?persistentId=hdl:11272.1/AB2/Y5KQNB/AQJTT9&version=1.1
https://abacus.library.ubc.ca/dataset.xhtml?persistentId=hdl:11272.1/AB2/YQFWCH

Here are the steps you got to follow:

1. Load your data into Arc. First, grab Buildings_1 and DEM_1m.tif
2. Create a hillshade to better understand the location.
3. Search up the Raster Solar Irradiation tool
    DEM_1m w/ a mask
4. Lets eliminate some of the non-suitable rooftops - https://natural-resources.canada.ca/sites/nrcan/files/canmetenergy/files/pubs/SolarReadyGuidelines_en.pdf

    90 d to 270 d
    angles below 60d
    greater than 10m^2 area

5. Use the "Con" SA tool to remove anything with a steep slope and north aspect
    Slope < 60
    22.5 < Aspect 337.5
    Output > 800

6. Use zonal statistics to investigate each roof individually
    Mask with buildings and use our filtered power potential
    Join it back into the building footprints

7. Make a selection to select all the buildings w/ a certain total area of usable rooftop