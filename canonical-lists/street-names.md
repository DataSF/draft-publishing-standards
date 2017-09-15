## Definition

_[Per Administrative Bulletin 035 (AB-035) in the San Francisco Building Codes](http://library.amlegal.com/nxt/gateway.dll/California/sfbuilding/buildingcode2016edition/administrativebulletins?f=templates$fn=default.htm$3.0$vid=amlegal:sanfrancisco_ca$anc=JD_AB-035)_:

> All primary entrances from the street to all buildings and all direct entrances from the street to separate tenant spaces or dwelling units shall be numbered

### Illustration

### Authority

* The official street numbers are assigned by the [Department of Building Inspection](http://sfdbi.org/) Building Official prior to permits for new structures according to the procedure in [AB-035](http://library.amlegal.com/nxt/gateway.dll/California/sfbuilding/buildingcode2016edition/administrativebulletins?f=templates$fn=default.htm$3.0$vid=amlegal:sanfrancisco_ca$anc=JD_AB-035)

## Use

* To identify addresses where precision is a requirement
* As a location identifier for a number of citywide business processes including noticing, permitting, business registrations, etc.

### Accepted values
* Street numbers are assigned according to rules laid out in AB-035, these specify:
  * The start and end point of address assignment
  * How many addresses are allocated between intersections and where that differs
  * Where even and odd numbers are assigned
* Any values in the Enterprise Addressing System have been entered by staff according to these rules
* If you believe there's been an error or a missing address, please ????

  
## Reference

| Dataset | Description and Constraints | Street Number Column |
| :--- | :--- | :--- |
| [Addresses - Enterprise Addressing System](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Addresses-Enterprise-Addressing-System/sr5d-tnui) | The EAS is the system of record for DBI when assigning official addresses. Associated coordinates are most often associated with the center of a parcel or close to it, rather than at the door or entry. This still allows associations, but it means that in certain cases a building footprint cannot be spatially matched with it's addresses. | `address_number` |

### Is anything wrong, unclear, missing?

[Leave a comment.](https://github.com/DataSF/draft-publishing-standards/issues/new?title=Comment:Street-Names&body=Comment:Street-Names)
