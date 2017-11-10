# Supervisor Districts

## Definition

* There are 11 members of the [Board of Supervisors](http://www.sfbos.org/), each representing a geographic district. 

### Illustration

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

## Use

* Primarily used for reporting by supervisor district

## Accepted values

* Column name should be `Supervisor District` or `supervisor_district`
* Values between 1 and 11 \(integer\)
* Acceptable ways to indicate no district include:
  * `null` meaning the field has no value
  * `-1` or `0` 
  * Indicate how no district is represented in your data dictionary
  * For example, [not all 311 cases](https://data.sfgov.org/City-Infrastructure/Case-Data-from-San-Francisco-311-SF311-/vw6y-z8j6) have a location and won't have an associated district

## Reference Datasets

@TODO: put in table format

* [Those supervisor districts](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Current-Supervisor-Districts/qr9q-k4m2) are a common boundary of interest to those doing citywide analysis.



