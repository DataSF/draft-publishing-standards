# Building Footprints

## Definition

* The envelope of a building in 2 dimensional space

### Illustration

### Authority

* SFGIS in the Department of Technology manages data collection and processing from LIDAR
  * LIDAR data is provided by a third-party and is updated every ???
  * From this data, SFGIS derives the footprints and assigns unique identifiers
* Information about buildings is captured by other departments including Building Inspection, SF Environment, SF Planning and the City's Real Estate Division among others.
  * Building footprints do not include administrative data about a building, but can be related to those data spatially and via unique identifiers

## Use

* To relate other administrative records to a structure
* To clarify among administrative datasets what specific structure is being referenced
* To improve the addressing model so that address numbers reference a building, not just a parcel

### Accepted values

* Footprints are not currently updated as new buildings are constructed
* For those buildings constructed before X, you can use the unique identifier `sf16_bldgid`
* For buildings that don't exist but should, please ????

### Reference

| Dataset | Description and Constraints | Block Column | Lot Column | APN Column |
| :--- | :--- | :--- | :--- | :--- |
| [Current Subdivision Parcels](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Subdivision-Parcels-aka-City-Lots-/45et-ht7c) | These are the current active recorded parcels. The geography can be used as reference but should not be used for anything requiring precision. | `block_num` | `lot_num` | `blklot` |
| [Recorded Parcel Geography with Transaction Date History](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Recorded-Parcel-Geography-with-Transaction-Date-Hi/3iun-6we5) | These are the current and historic parcels with recorded dates. Historic parcels only go back to about 1995 with some exceptions. Useful for tying historic administrative records to a location. The geography can be used as reference but should not be used for anything requiring precision. | `block_num` | `lot_num` | `blklot` |
| [San Francisco Assessor Blocks](https://data.sfgov.org/Geographic-Locations-and-Boundaries/San-Francisco-Assessor-Blocks/ndp2-nsue) | Just the blocks without lots | `block_num` | N/A | N/A |


