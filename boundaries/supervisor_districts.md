# Supervisor Districts

There are 11 members of the [Board of Supervisors](http://www.sfbos.org/), each representing a geographic district. [Those supervisor districts](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Current-Supervisor-Districts/gq7k-pfb2) are a common boundary of interest to those doing citywide analysis. Historically, there have been many ways of representing these districts in datasets. We are standardizing these fields so that the name will always be `Supervisor District` \(or `supervisor_district`\). The record will indicate the number of the district without any leading text.

**For Example:**

| Other Fields | Supervisor District |
| --- | --- |
| ... | 1 |
| ... | 2 |
| ... | 3 |
| ... | 4 |
| ... | 5 |
| ... | 6 |
| ... | 7 |
| ... | 8 |
| ... | 9 |
| ... | 10 |
| ... | 11 |

## Acceptable values for no district

Sometimes a dataset doesn't have accurate geographic information or there just isn't a relevant location for the record. For example, [not all 311 cases](https://data.sfgov.org/City-Infrastructure/Case-Data-from-San-Francisco-311-SF311-/vw6y-z8j6) have a location.

* Acceptable ways to indicate no district include
  * `null` meaning the field has no value
  * `-1` or `0` 
* Please indicate how no district is represented in your data dictionary



