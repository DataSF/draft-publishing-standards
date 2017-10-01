# Parcels

## Definition

* A parcel is a contiguous piece of owned land \(real property\) identified by a unique Assessor Parcel Number (APN)
* The APN is comprised of a **block number** and a **lot number**
  * Blocks are contiguous groups of lots bounded by streets or other features on all sides
    * Blocks can be split in the middle by other streets
  * Lots are sub-divided within the blocks
    * Lots also referred to as parcels
  * The City is broken up into over 6,000 blocks and over 200,000 individual lots

### Illustration

![](/assets/block_lots.png)

* Block 117 above is bounded:
  * On the North and South by Union and Green Streets
  * On the East and West by Stockton and Powell Streets
* Columbus Avenue bisects it, but both sides are still part of the same block
* The block is subdivided into lots numbered from 1 through 21 below
* A full Assessor Parcel Number would be the concatenation of the block and lot padded with zeroes as necessary
  * Blocks are 4 digits with an optional suffix - 117 becomes 0117
  * Lots are 3 digits with an optional suffix - 4 becomes 004
  * The full APN for lot 4 in block 117 is [0117004](http://propertymap.sfplanning.org?search=0117004)
* These are [recorded in paper maps](http://sfplanninggis.org/BlockBooks/AssessorBlock0117.pdf) in the Office of the Assessor Recorder and digitized
  * Digital versions below under reference

### Authority

* Recordation of final parcel maps happens with the Office of the Assessor-Recorder 
* Before recordation, subdivision maps are approved by the County Surveyor, the Public Works Director and the Board of Supervisors
  * More information about the [subdivision process and related codes on the Public Works website](http://sfpublicworks.org/services/subdivisions-and-mapping)

## Use

* To tie deeds and legal records to a property mapped [through an official land subdivision process](http://sfpublicworks.org/services/subdivisions-and-mapping)
* To assess and collect taxes on land and improvements 
* As a common administrative identifier for a number of processes like permitting

### Accepted values

* Should be provided in a dataset as at least 2 separate fields:
  * Block as `blk` or `block` or `block_num`
  * Lot as `lot` or `lot_num`
* When representing the fully qualified APN as a single field:
  * Name the column either `apn` or `assessor_parcel_number` or `blklot` or `block_and_lot`
  * Concatenate the block and lot together
  * Do not separate the block and lot number with space or other characters
    * 0585012D instead of 0585/012D
  * Do not prepend with additional text like `APN` or `Block and Lot Number`
  * Also provide the block and lot as separate fields
* Current parcels and corresponding identifiers in the current subdivision parcels
* Historic parcels and corresponding identifiers in the recorded parcel geography below (note limitations)

### Reference

| Dataset | Description and Constraints | Block Column | Lot Column | APN Column |
| :--- | :--- | :--- | :--- | :--- |
| [Current Subdivision Parcels](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Subdivision-Parcels-aka-City-Lots-/45et-ht7c) | These are the current active recorded parcels. The geography can be used as reference but should not be used for anything requiring precision. | `block_num` | `lot_num` | `blklot` |
| [Recorded Parcel Geography with Transaction Date History](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Recorded-Parcel-Geography-with-Transaction-Date-Hi/3iun-6we5) | These are the current and historic parcels with recorded dates. Historic parcels only go back to about 1995 with some exceptions. Useful for tying historic administrative records to a location. The geography can be used as reference but should not be used for anything requiring precision. | `block_num` | `lot_num` | `blklot` |
| [San Francisco Assessor Blocks](https://data.sfgov.org/Geographic-Locations-and-Boundaries/San-Francisco-Assessor-Blocks/ndp2-nsue) | Just the blocks without lots | `block_num` | N/A | N/A |

### Is anything wrong, unclear, missing?

[Leave a comment.](https://github.com/DataSF/draft-publishing-standards/issues/new?title=Comment:Parcels&body=Comment:Parcels)

