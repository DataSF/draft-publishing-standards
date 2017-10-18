# Date and Time

* [Based on ISO8601](https://en.wikipedia.org/wiki/ISO_8601), an international standard for representing date and time. We chose the "extended format" with the hyphens because it is more human readable.
  * Compare 2016-01-01 to 20160101
* All date and time variables must be local time (UTC -7hrs Standard Time UTC -8hrs Daylight Savings Time) unless specified.

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

* Fiscal year start-date must be indicated in the metadata

## Date-time and time variables
* ISO 8601 uses 24 hour clock system in hh:mm:ss format (do not use AM or PM)
* e.g. 13:00 is equivalent to 1:00 PM

| Type | Column name | Format | Example |
| --- | --- | --- | --- |
| Date + time | `date_time` | YYYY-MM-DD\[T\]hh:mm | 2015-01-01T13:00 |
| | | _or_ YYYY-MM-DD\[T\]hh:mm:ss | 2015-01-01T13:00:00 |
| Time only | `time` | hh:mm | 13:00 |
| | | _or_ hh:mm:ss | 13:00:00 |

**Specify the timezone if it is not local time (UTC -7hrs Standard Time UTC -8hrs Daylight Savings Time):**

| Type | Column name | Format | Example |
| --- | --- | --- | --- |
| Date + time | `date_time` | YYYY-MM-DD\[T\]hh:mm+hh:mm | 2015-01-01T12:00+00:00 |
| | | _or_ YYYY-MM-DD\[T\]hh:mm:ss+hh:mm:ss | 2015-01-01T12:00:00+00:00:00 |

## Date and time extracts

In certain cases you may want to provide a single variable representing the number or name of an individual date component, a day, a month, etc. There's no requirement to provide these, but follow this guidance:

| Extract | Column name | Type | Range of values |
| --- | --- | --- | --- | --- |
| Year | year_num | integer | any valid year |
| Month | month_num | integer | 1 to 12 |
| Month Name | month_name | string | January, February, March, April, May, June, July, August, September, October, November, December |
| Week of Year | woy_num | integer | 1 to 52 |
| Day | day_num | integer | 1 to 31 (varies by month) |
| Day of Week | dow_num | integer | 1 to 7 |
| Day of Week Name | dow_name | string | Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday |
| Hour | hour_num | integer | 1 to 24 |
| Minute | minute_num | integer | 1 to 60 |
| Second | second_num | integer | 1 to 60 |



These can often be automatically extracted from a date variable, for example the open data portal enables these queries:
* date_extract_d() - extracts the day from a date as an integer
* date_extract_dow() - extracts the day of week as an integer between 0 and 6 (inclusive)
* date_extract_hh() - extracts the hour of the day as an integer between 0 and 23 (inclusive)
* date_extract_m() - extracts the month as an integer
* date_extract_mm() - extracts the minute from the time as an integer 
* date_extract_ss() - extracts the second from the time as an integer
* date_extract_woy() - extracts the week of the year as an integer between 0 and 51 (inclusive)
* date_extract_y() - extracts the year as an integer

> **Note:** the functions above start counting at 0; when providing these fields in a dataset, start from 1 per the table above.



## Durations
Durations not required if you have a start and end date or datetime, however, if you produce a duration, follow the guidance below

### Is anything wrong, unclear, missing?

* should we specify column names for other common date table fields.  Like month alone '1' equals '2017-01.  Whats the standard naming convention for those? I want to update my  powerBI template's date table to match this standard

[Leave a comment.](https://github.com/DataSF/draft-publishing-standards/issues/new?title=Comment:Date-and-Time&body=Comment:Date-and-Time)

