# Supervisor Districts
There are 11 members of the [Board of Supervisors](http://www.sfbos.org/), each representing a geographic district. [Those supervisor districts](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Supervisor-Districts-as-of-April-2012/xz9b-wyfc) are a common boundary of interest to those doing citywide analysis. Historically, there have been many ways of representing these districts in datasets. We are standardizing these fields so that the name will always be *Supervisor District* (or supervisor_district). The record will indicate the number of the district without any leading text.

**For Example:**

| Other Fields | Supervisor District |
| -- | -- |
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

## Why is there a district 0 or no district?
Sometimes a dataset doesn't have accurate geographic information or there just isn't a relevant location for the record. For example, not all 311 calls have a location because some are people seeking information. In these cases, you'll find either a 0 or a blank value for Supervisor District.