# Street Centerlines and Nodes

## Definition
* Street centerlines are lines that represent a network of streets
  * They are aligned generally to the center of a street
  * They are meant to model the street network and thus have no width or area
  * They have a length component
* Street nodes are the endpoints of a street centerline and represent intersections
  * A node shared among multiple intersecting street segments is an intersection
* Each node and centerline segment will have a unique Centerline Node Network (CNN) identifier
* The collection of Centerline Node Network identifiers are collectively known as "CNNs"
  
### Illustration

![](/assets/centerlines.png)

* Shows [3 streets (Stockton, Green and Columbus) at a point of intersection](http://bsm.sfdpw.org/mapviewer/?cnn=12212000,12213000,25351000,25352000,25352000,25353000,25365000,4294000,4295000,6453000,6454000)
* Each segment sits between two nodes
  * A segment ends where it intersects with another segment OR at the physical end of a street (a dead end)
  * Some segments will start and end at the same node
* Each segment and node has a CNN identifier pictured above
* Segments share the same node where they intersect
  * Node ID 25352000 in the middle is shared by 6 segments


### Authority

* The management of streets falls to different jurisdictions within the City
  * Public Works manages and maintains the majority of streets within the City 
  * The remaining are managed and maintained by other entities like Caltrans, Presidio Trust National Park and Parks & Recreation, [a summary of miles of streets by jurisdiction is available on the open data portal](https://data.sfgov.org/City-Infrastructure/Miles-Of-Streets/5s76-j52p)
* Basemap data including streets from various jurisdictions is maintained by [Public Works](http://sfpublicworks.org/)

## Use

* Centerline Node Network IDs (CNNs) are referenced in many datasets throughout the City (including but not limited to permits and inspections, project management and asset management systems) 
* Used to enhance data by adding location attributes, allowing disparate datasets to be mapped as well as compared for analysis
* To model the transportation network

### Accepted Values
* Every centerline and node will have a unique Centerline Node Network (CNN) identifier 
  * `cnn` as a number
  * `cnntext` as a text string
* CNN IDs (CNN) may be used in secondary columns as reference
  * For example:
    * `f_node_cnn` and `t_node_cnn` to indicate from and to nodes
  * When referencing a CNN, include clear definition in the data dictionary, and include `cnn` in the column name
* Valid IDs are in the reference datasets below

### Reference Datasets
| Dataset | Description and Constraints | Reference Columns |
| :--- | :--- | :--- |
| [List of Streets and Intersections](https://data.sfgov.org/Geographic-Locations-and-Boundaries/List-of-Streets-and-Intersections/pu5n-qu5c) | A list of street segments and intersections sorted by street name and ascending address number. This data set is based on the City's GIS basemap and contains CNN id numbers for each record. | `cnn` as number <br> For segments: `from_cnn` and `to_cnn` define the node IDs at each end |
| [San Francisco Basemap Street Centerlines](https://data.sfgov.org/Geographic-Locations-and-Boundaries/San-Francisco-Basemap-Street-Centerlines/7hfy-8sz8) | A geographic reference of the all basemap streets including centerline node network identifiers and jurisdictions | `cnn` as number <br> `cnntext` as text <br>`f_node_cnn` as the starting (from) node ID <br> `t_node_cnn` as the ending (to) node ID |
| [Street Segment and Intersection (CNN) Change Log](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Street-Segment-and-Intersection-CNN-Change-Log/amiw-iisi) | A list of Street Segment and Intersection (CNN) changes including new, dropped, realigned, divided and split records. | `oldcnn` as number <br> `newcnn` as number|

### Is anything wrong, unclear, missing?

[Leave a comment.](https://github.com/DataSF/draft-publishing-standards/issues/new?title=Comment:Street-Centerlines-and-Nodes&body=Comment:Street-Centerlines-and-Nodes)



