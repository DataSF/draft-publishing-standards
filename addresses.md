# Location \(addresses\)

* Where appropriate, use the Enterprise Address System addresses

We'll accept a handful of formats for addresses. What is most important is that the component parts of an address that are relevant to the data are standard and well-formed.

You may output these as individual fields or as full address strings. When formatting as one field, it is still important to make sure the component pieces are well formed within the string.

## Address components

Below are components of an address. 
 - make sure the individual components of an address comply with the guidance below
 - you can publish addresses as either single strings or break into separate fields

| Component Name | Data Type | Definition | When to use |
| :--- | :--- | :--- | :--- |
| From Street | Numeric |  First part of a range: **1000**-1100 Main Street, San Francisco, CA 94102 | When the record location is associated with a range of addresses |
| To Street | Numeric | Second part of a range: 1000-**1500** Main Street, San Francisco, CA 94102 | When the record location is associated with a range of addresses |
| Street Number | Numeric | The precise address number; e.g in 315 Main Street, 315 is the Street Number | When the record location is associated with a specific address |
| Street Number Suffix | Text | The letter following a street number; e.g. 315A Main Street, A is the Street Number Suffix | When there is a letter following the street number |
| Street Name | Text | Just the street name, excluding type; e.g. 315 Main Street, Main is the Street Name | Always |
| Street Type | Text | Just the street type following the name; e.g. 315 Main Street, Street is the type | Always |
| Unit | Numeric | The unit number, for example if the address refers to an apartment; e.g 315 Main Street, Unit 2; 2 is the Unit | When the record location has a numeric unit associated with it |
| Unit Suffix | Text | The non-numeric component of a unit; e.g 315 Main Street, Unit 2A; A is the Unit Suffix; if no numeric portion of unit present, then this is the where the unit info goes; e.g. 315 Main Street, Unit B; B is the Unit Suffix \(Unit would be empty\) | When the record location has a letter following the numeric unit OR the unit is just a letter |
| City | Text | The city the address sits within; e.g. 315 Main Street, San Francisco CA | When the city is useful to differentiate among addresses; if all addresses are in one City, you can leave out and document that in the metadata |
| State | Text |  | When the state is useful to differentiate among addreses; if all addresses are in one State, you can leave out and document that in the metadata |
| Zipcode | Numeric |  | Always |

## Address formats

100 Van Ness Ave Unit 316A, San Francisco, CA 94102

