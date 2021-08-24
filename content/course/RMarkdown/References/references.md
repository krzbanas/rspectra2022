---
title: References
linkTitle: References
summary: References
date: '2021-01-24'
weight: 30
type: book
---


## What you will learn

Basics of R Markdown for manuscripts preparation in R.

## Courses in this program

{{< list_children >}}


## References

* references are defined in .bib files
* pandoc can process a citation only if there is a linked entry in the .bib file
* A BibTeX entry consists of three elements: a type (@article), a citation-key (banas2021), a number of tags (title, author)
* one could create entries by hand, a good alternative is to use Google Scholar, which provides BibTeX entries or JabRef, Zotero, Mendeley
* Reference styles are defined in .csl files files for different styles (e.g., APA) are available at https://www.zotero.org/styles
* .csl files are specified with the csl variable in YAML
* if unspecified, it uses a Chicago author-date format
* All citations keys take the 'at' sign @ while square brackets and/or minus signs introduce variation [@bennett2015] [@bennett2015 33-35]
* The list of references appears after the last line of the document, with no section header
* For internal links from in-text citations to the reference list, set link-citations: yes in YAML








