# Statistics on Digitized Newspapers

This directory contains informaiton on the dates, page counts, and character counts of digitized newspapers compiled for the [_Viral Texts_](https://viraltexts.org/) project.  Information is organized by `series`, a unique identifier for a newspaper, derived from the Library of Congress control number (as in [_Chronicling America_](https://chroniclingamerica.loc.gov/) and some other collections) or from internal collection identifiers.

## `dates.csv`

For quick comparisons, `dates.csv` provides simple minimum and maximum dates for newspaper series contained in various corpora.  For more finegrained issue counts per year, see `pages.csv` below.

Field | Description
---- | ----
`series` | unique identifer for the newspaper series
`corpus` | short identifier for the corpus; expanded forms are in `../corpora.csv`
`startDig` | date of earliest digitized issue
`endDig` | date of latest digitized issue

## `pages.csv`

This table contains information about the distribution of issue formats for each digitized newspaper series in each year.  Information for digitized papers from different corpora (e.g., _Chronicling America_, or the Internet Archive) is listed separately.  For each series-year, we show the count of issues with particular page counts, section counts, and section collations.  The section data, which is only available for the _Chronicling America_ data, is summarized as a series of the page counts in each section, separated by a `+` character.  For example, the collation `4+1` indicates a four-page section followed by a single sheet.

Field | Description
---- | ----
`series` | unique identifer for the newspaper series
`corpus` | short identifier for the corpus; expanded forms are in `../corpora.csv`
`year` | year with digitized data
`pp` | total pages in an issue
`sections` | number of sections in an issue
`collation` | sequence of page counts in each section, separated by `+` characters
`count` | number of issues in that series-year with the given pp/section/collation

## `output.csv`

This table contains information on the total digitized output&mdash;in issues, pages, and OCR-transcribed characters&mdash;for a given newspaper series in a given year.  We also show the date of the earliest and last digitized issues and the number of days between them.  This allows us, for newspapers that were only issued or digitized for part of the year, to estimate more accurately the rate of publication output per day.

Field | Description
---- | ----
`series` | unique identifer for the newspaper series
`year` | year with digitized data
`issues` | digitized issues from that series-year
`startDig` | date of the earliest digitized issue in that year
`endDig` | date of the latest digitized issue in that year
`days` | number of days difference between startDig and endDig
`pp` | total pages published in that year
`chars` | total characters of text digitized in that year
`empties` | number of undigitized pages in that year
`sdchars` | sample standard deviation of characters per issue
