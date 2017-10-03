# Building Footprints

## Definition

* The extent of a building in 2 dimensional space
* Includes a unique identifier and other information derived from LIDAR (e.g. max height)

### Illustration

![Building footprints are the extent or envelope of a building structure. Here they are pictured in 3D and 2D for the same block on Green Street. ](/assets/footprints.png)

* On left: Oblique view of Green St facing north between Columbus and Powell ( Imagery: &copy; 2017 Google; Left Panel Map Data: &copy; 2017 Google)
* On right: building footprints for the same block

### Authority

* SFGIS in the [Department of Technology](https://tech.sfgov.org/) manages data collection and processing from LIDAR
  * LIDAR data is provided by a third-party and is updated every ???
  * From this data, SFGIS derives the footprints and assigns unique identifiers as well as additional derived statistics about the building (e.g. min, max and median height)
* Information about buildings is captured by other departments including Building Inspection, SF Environment, SF Planning and the City's Real Estate Division among others.
  * Building footprints do not include administrative data about a building
  * They can be related to administrative data spatially and via unique identifiers

## Use

* To relate other administrative records to a structure
* To clarify among administrative datasets what specific structure is being referenced
* To improve the addressing model so that address numbers reference a building, not just a parcel

### Accepted values

* Footprints are not currently updated as new buildings are constructed
* For those buildings constructed before X, you can use the unique identifier `sf16_bldgid`
* For buildings that don't exist but should, please @TODO: what action can people take?

### Reference

| Dataset | Description and Constraints | Reference Columns |
| :--- | :--- | :--- | :--- | :--- |
| [Building Footprints](https://data.sfgov.org/Housing-and-Buildings/Building-Footprints/72ai-zege) | The footprint extents are collapsed from an earlier 3D building model provided by Pictometry of 2010, and have been refined from a version of building masses publicly available on the open data portal for over two years. The building masses were manually split with reference to parcel lines, but using vertices from the building mass wherever possible. These split footprints correspond closely to individual structures even where there are common walls; the goal of the splitting process was to divide the building mass wherever there was likely to be a firewall. An arbitrary identifier was assigned based on a descending sort of building area for 177,023 footprints. The centroid of each footprint was used to join a property identifier from a draft of the San Francisco Enterprise GIS Program's cartographic base, which provides continuous coverage with distinct right-of-way areas as well as selected nearby parcels from adjacent counties. | `sf16_bldgid` unique identifier for footprint <br> `mblr` for reference to property identifiers including parcels and right of way  |

### Is anything wrong, unclear, missing?

[Leave a comment.](https://github.com/DataSF/draft-publishing-standards/issues/new?title=Comment:Building-Footprints&body=Comment:Building-Footprints)