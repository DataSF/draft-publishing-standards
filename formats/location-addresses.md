# Location \(addresses\)

* Consistent formatting of addresses is important in the promotion of data use and reuse
* There are a couple of ways to output a valid address:
  * As individual fields
  * As a single complete address string
* The specific output may vary by the use case and underlying data
* Please review the address elements below and when they apply to your data, use the individual element guidance for consistency and quality
* Following are the address elements and some brief notes on formats

## Address elements

Below are some common elements of an address (but not all)

* not all addresses will have all elements
* address granularity will be driven by the business need, so not all systems will collect every element
* make sure the individual elements of an address line up with the guidance below
* you can publish addresses as either single strings or break into separate fields
  * provide this information in your data dictionary and be consistent

> **Note:** this guidance is provided to promote consistency across shared tabular datasets and not as a comprehensive guide to address standards. For a comprehensive standard on addressing, see the [Federal Geographic Data Committee (FGDC) United States Thoroughfare, Landmark, and Postal Address Data Data Standard](https://www.fgdc.gov/standards/projects/address-data)

| Element | Data Type | Definition | Valid Values |
| :--- | :--- | :--- | :--- |
| From Address Number | Numeric | First part of a range: **1000**-1100 Main Street, San Francisco, CA 94102 | [For each street centerline](https://data.sfgov.org/Geographic-Locations-and-Boundaries/San-Francisco-Basemap-Street-Centerlines/7hfy-8sz8) on the right side: `rt_fadd`; on the left side: `lf_fadd` |
| To Address Number | Numeric | Second part of a range: 1000-**1500** Main Street, San Francisco, CA 94102 | [For each street centerline](https://data.sfgov.org/Geographic-Locations-and-Boundaries/San-Francisco-Basemap-Street-Centerlines/7hfy-8sz8) on the right side: `rt_fadd`; on the left side: `lf_fadd` |
| Address Number Prefix | Numeric | The portion of the Complete Address Number that precedes the Address Number itself: **B**315 Main Street, San Francisco, CA 94102 | Official address numbers available through the [Enterprise Address System](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Addresses-Enterprise-Addressing-System/sr5d-tnui) as `address_number` |
| Address Number | Numeric | The numeric identifier for a land parcel, house, building, or other location along a thoroughfare or within a community: **315**A Main Street, San Francisco, CA 94102 | Official address numbers available through the [Enterprise Address System](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Addresses-Enterprise-Addressing-System/sr5d-tnui) as `address_number` |
| Address Number Suffix | Text | The portion of the Complete Address Number that follows the Address Number itself: 315 **A** Main Street, San Francisco, CA 94102 | Official address numbers available through the [Enterprise Address System](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Addresses-Enterprise-Addressing-System/sr5d-tnui) as `address_number_suffix` |
| Street Name Pre Modifier | Text | A word or phrase in a Complete Street Name that 1. Precedes and modifies the Street Name, but is separated from it by a Street Name Pre Type or a Street Name Pre Directional or both, or 2. Is placed outside the Street Name so that the Street Name can be used in creating a sorted (alphabetical or alphanumeric) list of street names.: 315A **Old** Main Street, San Francisco, CA 94102 | [Official list of street names maintained by Public Works](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Street-Names/6d9h-4u5v) |
| Street Name Predirectional | Text | A word preceding the street name that indicates the directional taken by the thoroughfare from an arbitrary starting point, or the sector where it is located: 315A **East** Main Street, San Francisco, CA 94102 | [Official list of street names maintained by Public Works](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Street-Names/6d9h-4u5v) |
| Street Name Pretype | Text | A word or phrase that precedes the Street Name and identifies a type of thoroughfare in a Complete Street Name: 315A Main **Street**, San Francisco, CA 94102 | [Official list of street names maintained by Public Works](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Street-Names/6d9h-4u5v) |
| Street Name | Text | The portion of the Complete Street Name that identifies the particular thoroughfare (as opposed to the Street Name Pre Modifier, Street Name Post Modifier, Street Name Pre Directional, Street Name Post Directional, Street Name Pre Type, Street Name Post Type, and Separator Element (if any) in the Complete Street Name.): 315A **Main** Street, San Francisco, CA 94102 | [Official list of street names maintained by Public Works](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Street-Names/6d9h-4u5v) |
| Street Name Posttype | Text | A word or phrase that follows the Street Name and identifies a type of thoroughfare in a Complete Street Name: 315A Main **Street**, San Francisco, CA 94102 | [Official list of street names maintained by Public Works](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Street-Names/6d9h-4u5v) |
| Street Name Postdirectional | Text | A word following the street name that indicates the directional taken by the thoroughfare from an arbitrary starting point, or the sector where it is located: 315A Main Street **East**, San Francisco, CA 94102 | [Official list of street names maintained by Public Works](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Street-Names/6d9h-4u5v) |
| Street Name Post Modifier | Text | A word or phrase in a Complete Street Name that follows and modifies the Street Name, but is separated from it by a Street Name Post Type or a Street Name Post Directional or both: 315A Main Street **Extended**, San Francisco, CA 94102 | [Official list of street names maintained by Public Works](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Street-Names/6d9h-4u5v) |
| Subaddress Type | Text | The type of subaddress to which the associated Subaddress Identifier applies. (Building, Wing, Floor, Apartment, etc. are types to which the Identifier refers.): 315A Main Street, **Apt** 2, San Francisco, CA 94102 | There is no complete reference of subaddresses (aka units) at the time. You can refer to [Enterprise Address System addresses with units for a partial list](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Addresses-with-Units-Enterprise-Addressing-System-/dxjs-vqsy). |
| Subaddress Identifier | Text | The letters, numbers, words, or combination thereof used to distinguish different subaddresses of the same type when several occur within the same feature: 315A Main Street, Apt **2**, San Francisco, CA 94102 | There is no complete reference of subaddresses (aka units) at the time. You can refer to [Enterprise Address System addresses with units for a partial list](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Addresses-with-Units-Enterprise-Addressing-System-/dxjs-vqsy). |
| City | Text | The city the address sits within: 315A Main Street, **San Francisco**, CA 94102 | |
| State Name | Text | The names of the US states and state equivalents: the fifty US states, the District of Columbia, and all U.S. territories and outlying possessions. A state (or equivalent) is "a primary governmental division of the United States." The names may be spelled out in full or represented by their two-letter USPS or ANSI abbreviation: 315A Main Street, San Francisco, **CA** 94102 | Recommend using standard abbreviations. Spell out if you can do so without introducing misspellings (e.g using validated entry). |
| ZIP code | Numeric | A system of 5-digit codes that identifies the individual Post Office or metropolitan area delivery station associated with an address: 315A Main Street, San Francisco, CA **94102** | Note, zip codes are not actually boundaries, but are defined by routes. A [list of valid San Francisco zipcodes can be downloaded here](https://data.sfgov.org/resource/srq6-hmpi.csv?$select=zip_code). |
| ZIP+4 | Numeric | A 4-digit extension of the 5-digit Zip Code (preceded by a hyphen) that, in conjunction with the Zip Code, identifies a specific range of USPS delivery addresses: 315A Main Street, San Francisco, CA 94102-**1212** | Note, zip codes are not actually boundaries, but are defined by routes. A [list of valid San Francisco zipcodes can be downloaded here](https://data.sfgov.org/resource/srq6-hmpi.csv?$select=zip_code). |

## Address formats

* Addresses should be output with the level of detail relevant to the data
  * e.g. permits can be applied down to the sub-address level
* If providing addresses in a complete string, make sure the addresses are well formed and consistent for easy parsing, for example:
  * 741 Ellis Street, Unit 5, San Francisco, CA 94109
  * 901 Bayshore Boulevard, Unit 209, San Francisco, CA 94124
* When providing multiple addresses within a dataset, be internally consistent with naming structure; prepend your column names with the type of address
  * e.g. address vs. mailing\_address (see [Registered Businesses dataset](https://data.sfgov.org/Economy-and-Community/Registered-Business-Locations-San-Francisco/g8m3-pdis/data))
* Where appropriate, use a valid Enterprise Address System address
  * EAS addresses capture addresses input by DBI staff, see the [section on address numbers for more detail](/basemap/address-numbers.md)

### Is anything wrong, unclear, missing?

[Leave a comment.](https://github.com/DataSF/draft-publishing-standards/issues/new?title=Comment:Location-Addresses&body=Comment:Location-Addresses)

