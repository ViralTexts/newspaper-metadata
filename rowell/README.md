# Rowell's Newspaper Directories

This directory contains data from [George P. Rowell and Companies _American Newspaper Directories_](https://www.loc.gov/rr/news/news_research_tools/ayersdirectory.html).

The structured data for the 1869 edition is based on [the copy hand-keyed by the Perseus Digital Library](https://github.com/gregorycrane/Perseus19cAmerican/blob/main/rowell.paper.ie.xml).  That data was normalized to ease information extraction.  We have tried to undo some of this normalization in the `head` and `contents` fields to more exactly match the printed edition, typos and all, so that it can be used for OCR training.

Entries with the same head are duplicated when they contain information about multiple editions of the same paper, e.g., a daily, tri-weekly, and weekly.  Each potentially has with its own size, price, page count, and circulation information, as well as links to separate library catalog records.

The `series` field, when present, links to records in the Library of Congress' [_US Newspaper Directory_](https://chroniclingamerica.loc.gov/).  As in that project, we preferentially link, when possible, to the catalog record for the physical volume rather than the microfilm or other media.  The `series` field contains `xref` for a cross-reference entry.  There are of course gaps in the USND.  For instance, if a daily edition is still extand but not a tri-weekly edition, there may only be a catalog record for the former.  Unlike the USND, Rowell and Co. also define _newspaper_ to include most magazines.  The USND does contain some magazines that made it past the library's initial filters, but they do not appear to be systematically included.

Linking records to the _US Newspaper Directory_ and correcting the transcription to more closely reflect the printed edition are works in progress.  Feel free to send pull requests.
