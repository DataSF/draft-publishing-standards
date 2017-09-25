# Street Centerlines and Nodes

## Definition
* Street centerlines are lines that represent street segments
  * They are aligned generally to the center of a street segment
  * They have no width and are meant to model the street network, not the extent of the street surface
* Street nodes are the endpoints of a street centerline
  * Intersecting streets will share nodes at the point of intersection
  
### Illustration


### Authority

* The management of streets falls to different jurisdictions within the City
  * Public Works manages the majority of street miles within the City 
  * The remaining are managed by other entities like Caltrans, Presidio National Park and Parks & Recreation, a summary of miles of streets by jurisdiction is available online
* Basemap data including streets from the various jurisdictions is maintained by Public Works

## Use

### Accepted Values
* Every centerline and node will have an identifier Centerline Node Network (CNN) ID 
  * `cnn` as a number
  * `cnntext` as a text string
* CNN IDs may be used in secondary columns to indicate the nodes that fall at the endpoints of a centerline
  * For example `f_node_cnn` and `t_node_cnn`
  




### Reference


