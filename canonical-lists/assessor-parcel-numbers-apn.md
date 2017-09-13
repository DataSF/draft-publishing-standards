# Assessor Parcel Numbers \(APN\)

## Definition

* The assessor parcel number is the unique identifier for a contiguous piece of owned land \(real property\)
* It is comprised of a **block number** and a **lot number**
  * Blocks are contiguous groups of lots bounded normally by streets on all sides
  * Lots are sub-divided within the blocks
  * The City is broken up into approximately XX blocks and over 200,000 individual lots

### Illustration

## Use

* To tie deeds and legal records to a property mapped [through an official land subdivision process](http://sfpublicworks.org/services/subdivisions-and-mapping)
* To assess and collect taxes on land and improvements 
* As a common administrative identifier for a number of processes like permitting

### Accepted values
* Should be provided in a dataset as at least 2 separate fields:
  * Block as `blk` or `block` or `block_num`
  * Lot as `lot` or `lot_num`
* When representing the fully qualified APN as a single field:
  * Concatenate the block and lot together
  * Do not separate the block and lot number with space or other characters
    * 1000015A instead of 1000/015A
  * Do not prepend with additional text like `APN` or `Block and Lot Number`
  * Also provide the block and lot separately for flexibility

## Examples

## Authority

* Recordation of final parcel maps happens with the Office of the Assessor-Recorder 
* Before being recorded, subdivision maps are approved by the County Surveyor, the Public Works Director and the Board of Supervisors
  * More information about the [subdivision process and related codes on the Public Works website](http://sfpublicworks.org/services/subdivisions-and-mapping)

## Reference

| Dataset | Description and Constraints | Block Column | Lot Column | APN Column |
| :--- | :--- | :--- | :--- | :--- |
| [Current Subdivision Parcels](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Subdivision-Parcels-aka-City-Lots-/45et-ht7c) | These are the current active recorded parcels. The geography can be used as reference but should not be used for anything requiring precision. | `blk` | `lot` | `blklot` |
| [Recorded Parcel Geography with Transaction Date History](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Recorded-Parcel-Geography-with-Transaction-Date-Hi/3iun-6we5) | These are the current and historic parcels with recorded dates. Historic parcels only go back to about 1995 with some exceptions. Useful for tying historic administrative records to a location. The geography can be used as reference but should not be used for anything requiring precision. | `blk` | `lot` | `blklot` |
| Assessor Blocks | Just the blocks without lots | `blk` | N/A | N/A |




