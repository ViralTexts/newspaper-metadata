# newspaper-metadata

Metadata, automatically and manually generated, about historical newspapers.

Currently, the JSON and CSV files contain the following fields:

Field | Description
---- | -----
`series` | unique identifier for a newspaper series, usually derived from existing identifiers such as LCCN numbers
`title` | title of series
`lang` | common languages in the series, according to catalogue data, a semicolon-delimited list
`publisher` | series publisher
`placeOfPublication` | listed place of publication
`corpora` | soure corpora, as a semicolon-delimited list
`coverage` | link to a https://dbpedia.org/ entry for the place of publication

