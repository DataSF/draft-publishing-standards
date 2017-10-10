# Location \(addresses\)

* Where appropriate, use the Enterprise Address System addresses
  * @@SFGIS: where should we send people to learn about EAS?
* You may output these as individual fields or as full address strings
  * When formatting as one field, it is still important to make sure the component pieces are well formed within the string.

## Address components

Below are components of an address.

* not all addresses will have all components
* address granularity will be driven by the business need, so not all systems will collect every component
* make sure the individual components of an address comply with the guidance below
* you can publish addresses as either single strings or break into separate fields; provide this information in your data dictionary and be consistent

| Component Name | Data Type | Definition | Valid Values |
| :--- | :--- | :--- | :--- |
| From Street | Numeric | First part of a range: **1000**-1100 Main Street, San Francisco, CA 94102 | [For each street centerline](https://data.sfgov.org/Geographic-Locations-and-Boundaries/San-Francisco-Basemap-Street-Centerlines/7hfy-8sz8) on the right side: `rt_fadd`; on the left side: `lf_fadd` |
| To Street | Numeric | Second part of a range: 1000-**1500** Main Street, San Francisco, CA 94102 | [For each street centerline](https://data.sfgov.org/Geographic-Locations-and-Boundaries/San-Francisco-Basemap-Street-Centerlines/7hfy-8sz8) on the right side: `rt_toadd`; on the left side: `lf_toadd` |
| Street Number | Numeric | The precise address number: **315**A Main Street, San Francisco, CA 94102 | Official address numbers available through the [Enterprise Address System](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Addresses-Enterprise-Addressing-System/sr5d-tnui) as `address_number` |
| Street Number Suffix | Text | The letter following a street number: 315**A** Main Street, San Francisco, CA 94102 | Official address numbers available through the [Enterprise Address System](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Addresses-Enterprise-Addressing-System/sr5d-tnui) as `address_number_suffix` |
| Street | Text | Just the street name, excluding type: 315A **Main** Street, San Francisco, CA 94102 | [Official list of street names maintained by Public Works](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Street-Names/6d9h-4u5v) |
| Street Type | Text | Just the street type following the name: 315A Main **Street**, San Francisco, CA 94102 | Either spell out or use the [Postal Service Standard Suffix Abbreviations](https://pe.usps.com/text/pub28/28apc_002.htm) |
| Unit | Numeric | The unit number, for example if the address refers to an apartment: 315A Main Street, Apt **2**, San Francisco, CA 94102 | There is no complete reference of units at the time. You can refer to [Enterprise Address System addresses with units for a partial list](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Addresses-with-Units-Enterprise-Addressing-System-/dxjs-vqsy). |
| Unit Suffix | Text | The non-numeric component of a unit, if there is one: 315A Main Street, Apt 2**A**, San Francisco, CA 94102; if no numeric portion of unit present: 315 Main Street, Apt **B**, San Francisco, CA 94102 \(Unit would be empty\) | There is no complete reference of units at the time. You can refer to [Enterprise Address System addresses with units for a partial list](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Addresses-with-Units-Enterprise-Addressing-System-/dxjs-vqsy). |
| City | Text | The city the address sits within: 315A Main Street, **San Francisco**, CA 94102 | You can leave this out if all addresses are consistently within the same City, but indicate this in your metadata |
| State | Text | The state the address sits within: 315A Main Street, San Francisco, **CA** 94102 | Recommend using standard state abbreviations. Spell out if you can do so without introducing misspellings. |
| ZIP code | Numeric | The address zipcode as defined by the USPS: 315A Main Street, San Francisco, CA **94102** | Note, zip codes are not actually boundaries, but are defined by routes. A [list of valid San Francisco zipcodes can be downloaded here](https://data.sfgov.org/resource/srq6-hmpi.csv?$select=zip_code). |

## Address formats

* Addresses should be output with the level of detail relevant to the data
  * e.g. permits can be applied down to the unit level; this information should be present where applicable
* If providing addresses in a single string, make sure the addresses are well formed and consistent for easy parsing
* When providing multiple addresses within a dataset, be internally consistent with naming structure; prepend your column names with the type of address
  * e.g. business\_address vs. mailing\_address vs. physical\_address

### Is anything wrong, unclear, missing?

[Leave a comment.](https://github.com/DataSF/draft-publishing-standards/issues/new?title=Comment:Location-Addresses&body=Comment:Location-Addresses)

