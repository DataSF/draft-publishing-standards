# Address Numbers

## Definition

[_Per Administrative Bulletin 035 \(AB-035\) in the San Francisco Building Codes_](http://library.amlegal.com/nxt/gateway.dll/California/sfbuilding/buildingcode2016edition/administrativebulletins?f=templates$fn=default.htm$3.0$vid=amlegal:sanfrancisco_ca$anc=JD_AB-035):

> All primary entrances from the street to all buildings and all direct entrances from the street to separate tenant spaces or dwelling units shall be numbered

### Illustration

![](/assets/address_numbers.png)

* Illustration of right side of Green Street between Columbus Ave and Powell St
* 100 valid address numbers on this segment from 600 to 699
  * Even adddresses on right, odds on left
* Each address corresponds to an entrance from the street
  * Note buildings at the rear of the building facing the street have entryways from the street (e.g. 656A, 658A, 664A, and 666A)
  * Numbers can be assigned where there is no building, but they must be associated [with a parcel](/basemap/assessor-parcel-numbers-apn.md)
    * e.g. the parking lot at 626 Green St


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
* Authorized City staff enter address numbers in the Enterprise Addressing System according to these rules

> **Note on Units:** The City records unit numbers for condos to support tying property records for deeds, property taxes and other business processes. There is no formal requirement to record the units in rental buildings.

> **Missing Data?:** If you believe there's been an error or a missing address, please @TODO: what feedback loop is there?

## Reference

| Dataset | Description and Constraints | Street Number Column |
| :--- | :--- | :--- |
| [Addresses - Enterprise Addressing System](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Addresses-Enterprise-Addressing-System/sr5d-tnui) | The EAS is the system of record for DBI when assigning official addresses. Associated coordinates are most often associated with the center of a parcel or close to it, rather than at the door or entry. This still allows associations, but it means that in certain cases a building footprint cannot be spatially matched via intersection or "point in polygon" with it's address\(es\). | `address_number` |
| [Addresses with Units - Enterprise Addressing System](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Addresses-Enterprise-Addressing-System/sr5d-tnui) | Same general limitations as the Addresses dataset above, but also includes sub-addresses like units. Unit numbers are formally referenced for condos because the City records these for the purposes of properly tying deeds and other property records to a specific unit and owner. Rental units are not formally recorded by the City. | `address_number` |

### Is anything wrong, unclear, missing?

[Leave a comment.](https://github.com/DataSF/draft-publishing-standards/issues/new?title=Comment:Street-Numbers-Addresses&body=Comment:Street-Numbers-Addresses)

