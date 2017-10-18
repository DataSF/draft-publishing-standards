# Location \(coordinates\)

@@SFGIS: is EPSG 2227 the right one for CA State Plane 3, is there a different one we should be standardizing around?

- Coordinates in [EPSG 4326](https://epsg.io/4326) or [EPSG 2227](https://epsg.io/2227)
- Only EPSG 4326 coordinates can be mapped within the open data portal
- Should be represented in two columns
    - EPSG 4326: `latitude` and `longitude` or 
    - EPSG 2227: `x_coord` and `y_coord`
    - **Note:** all EPSG 4326 coordinates will be loaded into the open data portal to support mapping and presented in an additional single location column there called `the_geom`. EPSG 2227 coordinates will be represented as the two original columns 
- In positive/negative floating point
    - e.g. `latitude`: 37.761146; `longitude`: -122.436235
- EPSG should be indicated in metadata

### Is anything wrong, unclear, missing?

[Leave a comment.](https://github.com/DataSF/draft-publishing-standards/issues/new?title=Comment:Location-Coordinates&body=Comment:Location-Coordinates)