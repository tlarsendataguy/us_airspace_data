[Object catalog](https://github.com/tlarsen7572/us_airspace_data#object-catalog) / elevation

## Ground elevation

**Note that this table is very large, almost 50 billion records. Do not attempt to download the entire table.**

Ground data is derived from elevation products provided by the United States Geological Survey (USGS). Specifically, the elevation table contains 1 arc-second resolution data points. This data is sourced from 1-degree by 1-degree geotiff files and covers most of North America.

Geotiff files encode elevation data into images. For 1 arc-second of resolution, each pixel represents the height of a plot of ground measuring 1 second of latitude and longitude. This translates to approximately 101 feet per latitude. Note that the length of a degree of longitude changes with latitude and will only be 101 feet at the equator.

Elevation data is stored in a simple table with 3 fields: Lon, Lat, and Elevation.

Lon and Lat are stored as tenths of a second. You can convert back to decimal degrees by dividing by 36,000. Each longitude and latitude represent the mid-point of the corresponding pixel. For example, assume a 1 arc-second pixel with its top-left corner at -100°W, 35°N. This translates to a box with the following coordinates:

|-3600000, 1260000|-3599990, 1260000|
|-----------------|-----------------|
|**-3600000, 1259990**|**-3599990, 1259990**|

The values stored in the elevation table for Lon and Lat will be -3599995 and 1259995.

Elevation is stored in meters above (or below) sea level.
