# Date and Time

* [Based on ISO8601](https://en.wikipedia.org/wiki/ISO_8601), an international standard for representing date and time. We chose the "extended format" with the hyphens because it is more human readable.
  * Compare 2016-01-01 to 20160101
* All date and time variables must be local time \(UTC -7hrs Standard Time UTC -8hrs Daylight Savings Time\) unless specified.

## Date variables

| Interval | Column name | Format | Range of values | Example |
| --- | --- | --- | --- | --- |
| Annual | `year` | YYYY | YYYY: 1776 onwards | 2015 |
| Monthly | `month` | YYYY-MM | MM: 01 to 12 | 2015-01 |
| Daily | `date` | YYYY-MM-DD | DD: 01 to 31 | 2015-01-01 |
| Weekly | `week` | YYYY-\[W\]WW | \[W\]WW: W01 to W52 | 2015-W01 |
| Quarterly | `quarter` | YYYY-\[Q\]Q | \[Q\]Q: Q1 to Q4 | 2015-Q1 |
| Half-yearly | `half_year` | YYYY-\[H\]H | \[H\]H: H1 or H2 | 2015-H1 |

**For fiscal periods, prefix “fiscal\_” to column name**

| Interval | Column name | Format | Example |
| --- | --- | --- | --- |
| Fiscal, annual | `fiscal_year` | YYYY | 2015 |
| Fiscal, monthly | `fiscal_month` | YYYY-MM | 2015-01 |
| Fiscal, quarterly | `fiscal_quarter` | YYYY-\[Q\]Q | 2015-Q1 |
| Fiscal, half-yearly | `fiscal_half_year` | YYYY-\[H\]H | 2015-H1 |

* Fiscal year start date must be indicated in the data dictionary
  * e.g. The fiscal year starts on July 1 and ends on June 30 for the City and County of San Francisco

## Date-time and time variables

* ISO 8601 uses 24 hour clock system in hh:mm:ss format \(do not use AM or PM\)
* e.g. 13:00 is equivalent to 1:00 PM

| Type | Column name | Format | Example |
| --- | --- | --- | --- |
| Date + time | `date_time` | YYYY-MM-DD\[T\]hh:mm | 2015-01-01T13:00 |
|  |  | _or_ YYYY-MM-DD\[T\]hh:mm:ss | 2015-01-01T13:00:00 |
| Time only | `time` | hh:mm | 13:00 |
|  |  | _or_ hh:mm:ss | 13:00:00 |

**Specify the timezone if it is not local time \(UTC -7hrs Standard Time UTC -8hrs Daylight Savings Time\):**

| Type | Column name | Format | Example |
| --- | --- | --- | --- |
| Date + time | `date_time` | YYYY-MM-DD\[T\]hh:mm+hh:mm | 2015-01-01T12:00+00:00 |
|  |  | _or_ YYYY-MM-DD\[T\]hh:mm:ss+hh:mm:ss | 2015-01-01T12:00:00+00:00:00 |

## Date and time extracts

In certain cases you may want to provide a single variable representing the number or name of an individual date component, a day, a month, etc. There's no requirement to provide these, but follow this guidance:

| Extract | Column name | Type | Range of values |
| :--- | :--- | :--- | :--- |
| Year | year\_num | integer | any valid year |
| Month | month\_num | integer | 1 to 12 |
| Month Name | month\_name | string | January, February, March, April, May, June, July, August, September, October, November, December |
| Week of Year | woy\_num | integer | 0 to 51 |
| Day | day\_num | integer | 1 to 31 \(varies by month\) |
| Day of Week | dow\_num | integer | 0 to 6 |
| Day of Week Name | dow\_name | string | Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday |
| Hour | hour\_num | integer | 0 to 23 |
| Minute | minute\_num | integer | 0 to 59 |
| Second | second\_num | integer | 0 to 59 |

These can often be automatically extracted from a valid ISO-8601 date, for example the open data portal enables querying a dataset with these date extract functions:

* [date\_extract\_d\(\)](https://dev.socrata.com/docs/functions/date_extract_d.html) - extracts the day from a date as an integer
* [date\_extract\_dow\(\)](https://dev.socrata.com/docs/functions/date_extract_dow.html) - extracts the day of week as an integer between 0 and 6 \(inclusive\)
* [date\_extract\_hh\(\)](https://dev.socrata.com/docs/functions/date_extract_hh.html) - extracts the hour of the day as an integer between 0 and 23 \(inclusive\)
* [date\_extract\_m\(\)](https://dev.socrata.com/docs/functions/date_extract_m.html) - extracts the month as an integer
* [date\_extract\_mm\(\)](https://dev.socrata.com/docs/functions/date_extract_mm.html) - extracts the minute from the time as an integer 
* [date\_extract\_ss\(\)](https://dev.socrata.com/docs/functions/date_extract_ss.html) - extracts the second from the time as an integer
* [date\_extract\_woy\(\)](https://dev.socrata.com/docs/functions/date_extract_woy.html) - extracts the week of the year as an integer between 0 and 51 \(inclusive\)
* [date\_extract\_y\(\)](https://dev.socrata.com/docs/functions/date_extract_y.html) - extracts the year as an integer

## Durations

Durations can be automatically calculated if you provide a separate start and end period in your dataset. If you also want to provide a duration, please:

* Provide the milliseconds between the start and end period (include the duration unit in the data dictionary)
  * Milliseconds can be rolled up to other time intervals
* Use duration in your column name but prepend with a useful descriptor, e.g:
  * flight\_duration
  * response\_duration
  * dwell\_time\_duration
  * travel\_duration
* Do not duplicate any of the duration column names per the [guidance on columns](/formats/column-headers.md)

> **Note:** ISO 8601 does have separate guidance on duration formatting, but we find this more cumbersome than just calculating milliseconds between a period for which there are many standard programming libraries.

### Is anything wrong, unclear, missing?

[Leave a comment.](https://github.com/DataSF/draft-publishing-standards/issues/new?title=Comment:Date-and-Time&body=Comment:Date-and-Time)

