# Street Names

## Definition

* The official street name assigned to a length of street through either the subdivision process or renaming
  * Street names are generally established during the development / subdivision of land [codified in the City's subdivision codes](http://library.amlegal.com/nxt/gateway.dll/California/subdivision/subdivisioncode?f=templates$fn=default.htm$3.0$vid=amlegal:sanfrancisco_ca$anc=JD_Subdivision)
  * Renaming streets can be initiated by members of the public or the Board of Supervisors [according to the process documented by Public Works](http://sfpublicworks.org/services/establishing-street-names)

### Illustration![](http://sfpublicworks.org/sites/default/files/dscn1226.jpg)

### Authority
* New street names are assigned during the development / subdivision of land
  * Recordation of final parcel maps, including any new streets happens with the Office of the Assessor-Recorder 
  * Before recordation, subdivision maps are approved by the County Surveyor, the Public Works Director and the Board of Supervisors

## Use

* For official base maps to label the streets properly
* As a component of a full address when appropriate

### Accepted values

* Official street names are maintained in the City's Official Basemap updated by Public Works staff
* The full list of valid City street names is [available in the street names dataset](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Street-Names/6d9h-4u5v)

### Reference

| Dataset | Description and Constraints | Reference Columns |
| :--- | :--- | :--- |
| [Street Names](hhttps://data.sfgov.org/Geographic-Locations-and-Boundaries/Street-Names/6d9h-4u5v) | Contains a list of officially valid street names contained in the City's Basemap | `fullstreetname` composed of `streetname` & `streettype` |
| [San Francisco Basemap Street Centerlines](hhttps://data.sfgov.org/Geographic-Locations-and-Boundaries/Street-Names/6d9h-4u5v) | A geographic reference of the all basemap streets including a number of street components like the valid name | `streetname` composed of `street` & `st_type` |

### Is anything wrong, unclear, missing?

[Leave a comment.](https://github.com/DataSF/draft-publishing-standards/issues/new?title=Comment:Street-Names&body=Comment:Street-Names)

