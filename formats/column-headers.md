# Column Headers

* Only use alphanumeric or these 3 special characters: period \(.\), dash \(-\), and underscore \(\_\)
  * Ampersand \(&\) should be replaced by “and” if needed
* Each must be unique
  * Can’t have two headers called "duration"
* Units of measure should be omitted
  * Units can and should be provided with the data dictionary
* Keep short \(less than 30 characters\)
  * A full description can and should be provided with the data dictionary

# Column Order

* _Unique identifiers_ should be in the left-most column if applicable
* _Date and time variables_ should be in the first column for time series data
* _Fixed or classified variables_ should be ordered with the highest-level variable on the left and most granular variable on the right, for example
  * [311 cases](https://data.sfgov.org/City-Infrastructure/311-Cases/vw6y-z8j6/data): service_name, service_subtype, service_details
  * [Police incidents](https://data.sfgov.org/Public-Safety/Police-Department-Incidents/tmnf-yvry/data): category, descript
* _Observed variables_ should always be on the rightmost columns



### Is anything wrong, unclear, missing?

-Some explanation/example of what fixed and observed variables are

* for non timeseries data I would put unique identifier on the far left.



[Leave a comment.](https://github.com/DataSF/draft-publishing-standards/issues/new?title=Comment:Column-Headers-Order&body=Comment:Column-Headers-Order)

