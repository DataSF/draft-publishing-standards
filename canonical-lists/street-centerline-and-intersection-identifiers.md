# Street Centerlines and Nodes

## Definition
* Street centerlines are lines that represent street segments
  * They are aligned generally to the center of a street segment
  * They have no width and are meant to model the street network, not the extent of the street surface
* Street nodes are the endpoints of a street centerline
  * Intersecting streets will share nodes at the point of intersection
* Every centerline and node will have an identifier Centerline Node Network (CNN) ID 
  * `cnn` as a number
  * `cnntext` as a text string
* CNN IDs may be used in secondary columns to indicate from and to
  * `f_node_cnn` and `t_node_cnn`
  


