# Best Practices in Geospatial Data

Geospatial data are often stored in a complex proprietary format (e.g. ESRI geodatabase) that is extremely difficult to archive for long-term preservation and access. A single geodatabase can contain many individual data sets. Each individual data set, within a geodatabase, typically consists of multiple individual files (in proprietary formats) that record the spatial information, attribute information, and other essential database properties required to use the data. The complexity of the geodatabase (e.g. a few individual feature classes or many feature classes with related tables and attribute domains) will determine the best methods to use when creating open data formats for archival purposes. Please consult with your program Data Manager and/or GIS Analyst, prior to archiving geospatial data. Broad steps for managing geospatial data include:

* Fully document each individual feature class or shapefile.
* Store individual geodatabases and shapefiles in the archive folder directory structure as with other data types.
* Convert the geodatabase or shapefile to an open format (e.g. [GeoPackage](https://en.wikipedia.org/wiki/GeoPackage)) and store in the archive folder.

Additional guidance relevant to this data type is currently under development.\
