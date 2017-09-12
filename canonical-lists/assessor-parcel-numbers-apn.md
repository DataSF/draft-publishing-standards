# Assessor Parcel Numbers \(APN\)

## Definition

* The assessor parcel number is the unique identifier for a contiguous piece of real property that is assigned ownership 
* It is comprised of a block number and a lot number
  * Blocks are contiguous groups of parcels bounded normally by streets on all sides
  * Lots are sub-divided within the blocks
  * The City is broken up into approximately XX blocks and over 200,000 individual lots

This identifier is used to tie deeds and other legal records to a precise property mapped through a land subdivision process defined in local and state codes. It is also used to assess and collect taxes on land and improvements and is a common administrative identifier for a number of other processes.

## Authority

* Recordation of final parcels maps happens with the Office of the Assessor-Recorder 
* Before being recorded, subdivision maps must be approved by the County Surveyor, the Public Works Director and the Board of Supervisors
* More information about the [subdivision process and related codes on the Public Works website](http://sfpublicworks.org/services/subdivisions-and-mapping)

## Reference

| Dataset | Description and Constraints | APN Reference Column |
| :--- | :--- | :--- |
| [Current Subdivision Parcels](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Subdivision-Parcels-aka-City-Lots-/45et-ht7c) | These are the current active recorded parcels. The geography can be used as reference but should not be used for anything requiring precision. | `blklot` |
| [Recorded Parcel Geography with Transaction Date History](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Recorded-Parcel-Geography-with-Transaction-Date-Hi/3iun-6we5) | These are the current and historic parcels with recorded dates. Historic parcels only go back to about 1995 with some exceptions. Useful for tying historic administrative records to a location. The geography can be used as reference but should not be used for anything requiring precision. | `blklot` |



