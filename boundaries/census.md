# Census Boundaries

Census data is available from the [Federal Census Bureau](http://census.gov). For certain City administrative datasets, we assign census boundaries to make linking these to Census data easier.

For census boundary IDs we present the full ID starting with State ID and going down to the most granular ID represented by the field \(e.g. tract, block or block group\). The full IDs are presented as strings, not numbers. You can learn more about geographic [boundaries and identifiers on the Census website](https://www.census.gov/geo/reference/geocodes.html). The full IDs are constructed in the following order:

```
State FIPS Code (2 digit) > County FIPS code (3 digit) > Tract ID (6 digit) > Blockgroup ID (1 digit) > Block ID (4 digits, but first digit is the same as Blockgroup ID)
```

On City datasets with a Census geography column, we only represent the ID for the most granular geography appropriate to the data. For example, if we publish down to the Census block, we don't include a separate column for blockgroup or tract. One can derive these from the full ID because of the nesting relationship mentioned above.

| Census Boundary | Example ID | Label |
| --- | --- | --- |
| State | 06 | California |
| County | 06075 | San Francisco County, California |
| Census Tract | 06075010100 | Census Tract 101, San Francisco County, California |
| Census Blockgroup | 060750101001 | Block Group 1, Census Tract 101, San Francisco County, California |
| Census Block | 060750101001000 | Block 1000, Block Group 1, Census Tract 101, San Francisco County, California |



