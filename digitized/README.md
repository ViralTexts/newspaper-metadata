# Statistics on Digitized Newspapers

## `dates.csv`

For quick comparisons, `dates.csv` provides simple minimum and maximum dates for newspaper series contained in various corpora.  For more finegrained issue counts per year, see `pages.csv` below.

The fields are:

Field | Description
---- | ----
`series` | unique identifer for the newspaper series, derived from LC control number (where available) or internal collection identifiers
`corpus` | short identifier for the corpus; expanded forms are in `../corpora.csv`
`startDig` | date of earliest digitized issue
`endDig` | date of latest digitized issue

## `pages.csv`

Field | Description
---- | ----
`series` | unique identifer for the newspaper series, derived from LC control number (where available) or internal collection identifiers
`corpus` | short identifier for the corpus; expanded forms are in `../corpora.csv`
`year` | year with digitized data
`pp` | total pages in an issue
`sections` | number of sections in an issue (only in Chronicling America, if at all)
`collation` | sequence of page counts in each section, separated by `+` characters
`count` | number of issues in that series-year with the given pp/section/collation

## `output.csv`


`Field | Description
---- | ----
`series` | unique identifer for the newspaper series, derived from LC control number (where available) or internal collection identifiers
`year` | year with digitized data
`issues` | digitized issues from that series-year
`startDig` | date of the earliest digitized issue in that year
`endDig` | date of the latest digitized issue in that year
`days` | number of days difference between startDig and endDig
`pp` | total pages published in that year
`chars` | total characters of text digitized in that year
`empties` | number of undigitized pages in that year
`sdchars` | sample standard deviation of characters per issue
