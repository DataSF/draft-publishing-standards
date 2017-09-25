# Street Centerlines and Nodes

## Definition
* Street centerlines are lines that represent street segments
  * They are aligned generally to the center of a street
  * They have no width and are meant to model the street network, not the extent of the surface
* Street nodes are the endpoints of a street centerline
  * Intersecting streets will share nodes at the point of intersection
  
### Illustration


### Authority

* The management of streets falls to different jurisdictions within the City
  * Public Works manages the majority of street miles within the City 
  * The remaining are managed by other entities like Caltrans, Presidio National Park and Parks & Recreation,[ a summary of miles of streets by jurisdiction is available on the open data portal](https://data.sfgov.org/City-Infrastructure/Miles-Of-Streets/5s76-j52p)
* Basemap data including streets from various jurisdictions is maintained by Public Works

## Use

* Centerline Node Network IDs as a reference in other geographic data like addresses or parcels
* To model the transportation network

### Accepted Values
* Every centerline and node will have an identifier Centerline Node Network (CNN) ID 
  * `cnn` as a number
  * `cnntext` as a text string
* CNN IDs may be used in secondary columns to indicate the nodes that fall at the endpoints of a centerline
  * For example `f_node_cnn` and `t_node_cnn`
  * When referencing a CNN, include clear definition in the data dictionary

### Reference
| Dataset | Description and Constraints | Reference Columns |
| :--- | :--- | :--- |
| [List of Streets and Intersections](https://data.sfgov.org/Geographic-Locations-and-Boundaries/List-of-Streets-and-Intersections/pu5n-qu5c) | A list of street segments and intersections sorted by street name and ascending address number. This data set is based on the City's GIS basemap and contains CNN id numbers for each record. | `cnn` as number <br> For segments: `from_cnn` and `to_cnn` define the node IDs at each end |
| [San Francisco Basemap Street Centerlines](hhttps://data.sfgov.org/Geographic-Locations-and-Boundaries/Street-Names/6d9h-4u5v) | A geographic reference of the all basemap streets including centerline node network identifiers and jurisdictions | `cnn` as number <br> `cnntext` as text <br>`f_node_cnn` as the starting (from) node ID <br> `t_node_cnn` as the ending (to) node ID |
| [Street Segment and Intersection (CNN) Change Log](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Street-Segment-and-Intersection-CNN-Change-Log/amiw-iisi) | A list of Street Segment and Intersection (CNN) changes including new, dropped, realigned, divided and split records. | `oldcnn` as number <br> `newcnn` as number|



