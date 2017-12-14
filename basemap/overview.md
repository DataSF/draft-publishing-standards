# Basemap Overview

## A location reference \(addressing\) data model

Each component is described in this section individually, but there are important relationships among them.

Let's start with three core components:

* [**Parcels**](/basemap/parcels.md). The most common unit of reference for City data, the parcel defines the physical extent of land ownership. It is the outcome of a regulated land subdivision process.
* [**Address Numbers**](/basemap/address-numbers.md). As an outcome of permitting, new address numbers are assigned to each entry from the street per rules specified in the Building Codes.
* [**Building Footprints**](/basemap/building-footprints.md). Building footprints represent a physical structure in 2D extents. These are not formally digitized and added to a reference during the development process.

> **Note:** at the time, because buildings are not updated as development occurs, there will be missing data.

### Illustration

The following illustrates the relationship among the components.

![](/assets/address_components_illustration.png)

1. **1 Parcel, 1 Building.** This is often the case in areas like the Financial District or other densely populated office districts.
2. **1 Parcel, Many Buildings.** This occurs in neighborhoods with accessory dwelling units or detached buildings.
3. **Many Parcels, 1 Building.** This occurs when a building is subdivided into different ownership.
4. **1 Parcel, No Buildings.** While rare, this does happen in the case of parking lots, vacant lots and some parks.
5. **No parcels, 1 Building.** Buildings can be built in the right of way \(e.g. on a median\) where parcels don't exist. This happens rarely.

In all cases, a single address can never be associated with multiple buildings or multiple parcels.

### Relationship table and conceptual diagram

The table and diagram below explain the relationship among the 3 core components above.

| From | To | Relationship | Notes |
| :--- | :--- | :--- | :--- |
| Address Number | Parcel | An address number is related to 0 or 1 parcel | An address number may only occasionally fall in the right of way where there is no parcel @SFGIS? is this true, I vaguely remember this being mentioned in the AWG, but I could be confusing this with virtual addresses |
| Address Number | Building | An address number is related to 0 or 1 building | In some cases an address will be assigned to a lot with no physical structure |
| Parcel | Address Number | A parcel has 0 or many address numbers | When a parcel is first created through subdivision, it may have no addresses associated with it yet |
| Parcel | Building | A parcel has 0 or many buildings | A parcel doesn't have to have a building on it |
| Building | Address Number | A building has 1 or many address numbers | Per Building Code, once a building is approved, it will have at least 1 entrance address if not more\* |
| Building | Parcel | A building is in 0 or many parcels | Buildings may actually exist in the roadway \(e.g. a public works toolshed\) and not sit on a parcel at all. Most buildings sit within 1 or many parcels. |

> **\*Note:** The relationship between buildings and address numbers is conceptual at the time. Staff create address points in the Enterprise Addressing System \(EAS\) within the parcel but not in reference to the building. In cases where there is one building on one parcel, the address point may fall within the building footprint, but there's not an explicitly modeled relationship across all buildings.

![](/assets/address_components.png)

### Relationship to streets

Each of these components relates to one or more streets. A street centerline has a unique identifier called a [Centerline Node Network ID](/basemap/street-centerlines-nodes.md).

* A building or parcel will relate to at least one street segment
  * Parcels or buildings with streets on either side will have 2 related segments
  * Corner buildings and parcels will also relate to two segments
  * Depending on the size and shape of the parcel or building, they could be fronted on several or all sides by street segments
  * Most parcels or buildings on the interior of a block will relate to a single street segment
* An address number can only be associated with a single street segment
  * When the City assigns an address number they do so [along a street segment within an allowed range](/basemap/address-numbers.md)

### A note on historical data

Streets, parcels, buildings, addresses all change over time. Historical City data could reference things that don't currently exist. In each of the next pages, references include both current and historical where available. You can also [browse the reference index](/reference-index.md).
