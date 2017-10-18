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
| Fiscal, monthly | `fiscal_month` |
| Fiscal, quarterly | `fiscal_quarter` | YYYY-\[Q\]Q | 2015-Q1 |
| Fiscal, half-yearly | `fiscal_half_year` | YYYY-\[H\]H | 2015-H1 |

* Fiscal year start-date must be indicated in the metadata

## Date

## Date-time variables
* ISO 8601 uses 24 hour clock system in hh:mm:ss format

| Type | Column name | Format | Example |
| --- | --- | --- | --- |
| Date + time | `date_time` | YYYY-MM-DD\[T\]hh:mm | 2015-01-01T12:00 |
|  |  | _or_ YYYY-MM-DD\[T\]hh:mm:ss | 2015-01-01T12:00:00 |
| Time only | `time` | hh:mm | 12:00 |
|  |  | _or_ hh:mm:ss | 12:00:00 |

**Specify the timezone if it is not UTC -7hrs:**

| Type | Column name | Format | Example |
| --- | --- | --- | --- |
| Date + time | `date_time` | YYYY-MM-DD\[T\]hh:mm+hh:mm | 2015-01-01T12:00+00:00 |
|  |  | _or_ YYYY-MM-DD\[T\]hh:mm:ss+hh:mm:ss | 2015-01-01T12:00:00+00:00:00 |

## Durations
Durations not required if you have a start and end date or datetime, however, if you produce a duration, follow the guidance below

### Is anything wrong, unclear, missing?

* should we specify column names for other common date table fields.  Like month alone '1' equals '2017-01.  Whats the standard naming convention for those? I want to update my  powerBI template's date table to match this standard

[Leave a comment.](https://github.com/DataSF/draft-publishing-standards/issues/new?title=Comment:Date-and-Time&body=Comment:Date-and-Time)

