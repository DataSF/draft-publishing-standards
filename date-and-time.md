# Date and Time
- [Based on ISO8601](https://en.wikipedia.org/wiki/ISO_8601), an international standard for representing date and time. We chose the "extended format" with the hyphens because it is humanly more readable.
- Compare 2016-01-01 to 20160101

- All date and time variables must be in UTC -7hrs unless specified.

- Date variables:

    | Interval    | Column name | Format     | Range of values    | Example   |
    |-------------|-------------|------------|--------------------|-----------|
    | Annual      | `year`      | YYYY       | YYYY: 1776 onwards | 2015      |
    | Monthly     | `month`     | YYYY-MM    | MM: 01 to 12       | 2015-01   |
    | Daily       | `date`      | YYYY-MM-DD | DD: 01 to 31       | 2015-01-01|
    | Weekly      | `week`      | YYYY-[W]WW | [W]WW: W01 to W52  | 2015-W01  |
    | Quarterly   | `quarter`   | YYYY-[Q]Q  | [Q]Q: Q1 to Q4     | 2015-Q1   |
    | Half-yearly | `half_year` | YYYY-[H]H  | [H]H: H1 or H2     | 2015-H1   |
    
- For fiscal periods, prefix “fiscal_” to column name:

    | Interval               | Column name           | Format    | Example |
    |------------------------|-----------------------|-----------|---------|
    | Fiscal, annual      | `fiscal_year`      | YYYY      | 2015    |
    | Fiscal, quarterly   | `fiscal_quarter`   | YYYY-[Q]Q | 2015-Q1 |
    | Fiscal, half-yearly | `fiscal_half_year` | YYYY-[H]H | 2015-H1 |

    - Fiscal year start-date must be indicated in the metadata

- For date-time variables:

    | Type        | Column name | Format                     | Example             |
    |-------------|-------------|----------------------------|---------------------|
    | Date + time | `date_time` | YYYY-MM-DD[T]hh:mm         | 2015-01-01T12:00    |
    |             |             | *or* YYYY-MM-DD[T]hh:mm:ss | 2015-01-01T12:00:00 |
    | Time only   | `time`      | hh:mm                      | 12:00               |
    |             |             | *or* hh:mm:ss              | 12:00:00            |

- Specify the timezone if it is not UTC -7hrs:

    | Type        | Column name | Format                     | Example               |
    |-------------|-------------|----------------------------|-----------------------|
    | Date + time | `date_time` | YYYY-MM-DD[T]hh:mm+hh:mm   | 2015-01-01T12:00+00:00|
    |             |             | *or* YYYY-MM-DD[T]hh:mm:ss+hh:mm:ss | 2015-01-01T12:00:00+00:00:00 |