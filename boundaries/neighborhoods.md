# Neighborhoods

@@Joy - let's chat about neighborhoods, I want to rewrite this to be a little more in line with other guidance, but I'm also considering changing some conventions based on feedback

The City's Open Data Program provides the [Analysis Neighborhoods](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Analysis-Neighborhoods/p5b7-5n3h) as the primary neighborhood district boundary on automated datasets. We will also provide other neighborhood boundaries when appropriate.

The table below includes:

* the name and link to each of the neighborhood districts
* the human readable column name used on the open data portal
* the application programming interface \(API\) name
* the shortname used when there are character limits \(e.g. in shapefile formats\)
* the number of districts included in the dataset
* a quick link to download a CSV of just the boundary names \(without geometry\)

| Dataset | Column Name \(Human Readable\) | API Name | Short Name | Number of Neighborhoods | Download Boundary Names |
| :--- | :--- | :--- | :--- | :--- | :--- |
| [Analysis Neighborhoods](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Analysis-Neighborhoods/p5b7-5n3h) | Neighborhooods - Analysis Boundaries | neighborhoods\_analysis\_boundaries | NBHDANA | 42 | [Download](https://data.sfgov.org/resource/xfcw-9evu.csv?$select=nhood) |
| [Neighborhood Groups](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Neighborhood-Groups-Map/iacs-ws63) | Neighborhoods - Group Boundaries | neighborhoods\_group\_boundaries | NBHDGRP | 37 | [Download](https://data.sfgov.org/resource/aivd-8yrg.csv?$select=neighborho) |
| [SF Realtor Neighborhoods](https://data.sfgov.org/Geographic-Locations-and-Boundaries/Realtor-Neighborhoods/5gzd-g9ns) | Neighborhoods - Realtor Boundaries | neighborhoods\_realtor\_boundaries | NBHDSFRA | 92 | [Download](https://data.sfgov.org/resource/743h-p4bq.csv?$select=nbrhood) |
| [SFFind Neighborhoods](https://data.sfgov.org/Geographic-Locations-and-Boundaries/SF-Find-Neighborhoods/pty2-tcw4) | Neighborhoods - SFFind boundaries | neighborhoods\_sffind\_boundaries | NBHDSFFIND | 117 | [Download](https://data.sfgov.org/resource/6ia5-2f8k.csv?$select=name) |

**Note:** Datasets published before we codified this practice may not reflect the above. We are actively improving existing datasets on a rolling basis. Please consult the data dictionary and other related documentation under the dataset's About tab. If it's still unclear, [contact DataSF](http://support.datasf.org/customer/portal/emails/new), and we'll be happy to help.

