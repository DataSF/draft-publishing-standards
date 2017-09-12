# Location \(addresses\)

* Where appropriate, use the Enterprise Address System addresses
* We'll accept a handful of formats for addresses. What is most important is that the component parts of an address that are relevant to the data are standard and well-formed.
* You may output these as individual fields or as full address strings. When formatting as one field, it is still important to make sure the component pieces are well formed within the string.

## Address components

Below are components of an address. 
 - not all addresses will have all components
 - make sure the individual components of an address comply with the guidance below
 - you can publish addresses as either single strings or break into separate fields; provide this information in your data dictionary

| Component Name | Data Type | Definition | Valid Values |
| :--- | :--- | :--- | :--- |
| From Street | Numeric |  First part of a range: **1000**-1100 Main Street, San Francisco, CA 94102 | [For each street centerline](https://data.sfgov.org/Geographic-Locations-and-Boundaries/San-Francisco-Basemap-Street-Centerlines/7hfy-8sz8) on the right side: `rt_fadd`; on the left side: `lf_fadd` |
| To Street | Numeric | Second part of a range: 1000-**1500** Main Street, San Francisco, CA 94102 | [For each street centerline](https://data.sfgov.org/Geographic-Locations-and-Boundaries/San-Francisco-Basemap-Street-Centerlines/7hfy-8sz8) on the right side: `rt_toadd`; on the left side: `lf_toadd` |
| Street Number | Numeric | The precise address number: **315**A Main Street, San Francisco, CA 94102 | Official address numbers available through the [Enterprise Address System](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Addresses-Enterprise-Addressing-System/sr5d-tnui) as `address_number`|
| Street Number Suffix | Text | The letter following a street number: 315**A** Main Street, San Francisco, CA 94102 | Official address numbers available through the [Enterprise Address System](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Addresses-Enterprise-Addressing-System/sr5d-tnui) as `address_number_suffix` |
| Street | Text | Just the street name, excluding type: 315A **Main** Street, San Francisco, CA 94102 | [Official list of street names maintained by Public Works](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Street-Names/6d9h-4u5v) |
| Street Type | Text | Just the street type following the name: 315A Main **Street**, San Francisco, CA 94102 | Either spell out or use the USPS valid abbreviations |
| Unit | Numeric | The unit number, for example if the address refers to an apartment; e.g 315A Main Street, Apt **2**, San Francisco, CA 94102| There is no complete reference of units at the time. You can refer to [Enterprise Address System addresses with units for a partial list](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Addresses-with-Units-Enterprise-Addressing-System-/dxjs-vqsy). |
| Unit Suffix | Text | The non-numeric component of a unit; e.g 315 Main Street, Unit 2A; A is the Unit Suffix; if no numeric portion of unit present, then this is the where the unit info goes; e.g. 315 Main Street, Unit B; B is the Unit Suffix \(Unit would be empty\) | When the record location has a letter following the numeric unit OR the unit is just a letter |
| City | Text | The city the address sits within; e.g. 315 Main Street, San Francisco CA | When the city is useful to differentiate among addresses; if all addresses are in one City, you can leave out and document that in the metadata |
| State | Text |  | When the state is useful to differentiate among addreses; if all addresses are in one State, you can leave out and document that in the metadata |
| Zipcode | Numeric |  | Always |

## Address formats

100 Van Ness Ave Unit 316A, San Francisco, CA 94102

