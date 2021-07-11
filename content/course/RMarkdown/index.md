---
title: R Markdown
linkTitle: RMarkdown
summary: R Markdown
date: '2021-01-24'
weight: 60
type: book
---


## What you will learn

Basics of R Markdown for manuscripts preparation in R.

## Courses in this program

{{< list_children >}}

R Markdown follows the syntax in Pandoc's Markdown

## Lines, paragraphs, headers

* Multiple spaces on a given line are reduced to one
* Line endings with fewer than two spaces are ignored
* Two or more spaces at the end of lines introduce hard breaks, forcing a new line
* Spaces in lines starting with a vertical line | are kept
* Lines starting with the greater-than sign > introduce block quotes
* One or more (multiple blank lines between paragraphs reduce to one) blank lines introduce a new paragraph
* Text with the syntax <!--comments --> is omitted from output
* The number sign # introduces headers; lower levels are created with additional signs — up to total five levels
* A pair of single asterisk * or underscores _ introduces italics
* A pair of double asterisk or underscores introduces bold
* These two rules can be combined
* A pair of double tildes ~ introduces strikethrough


## Links, footnotes, equations, lists

* link text to section headers in the same document [Conclusion](#conclusion)
* Multi-word headers need hyphenation [Literature Review](#literature-review)
* You can link text to URLs [visit my website](https://resulumit.com/) [email me](mailto:resuluy@uio.no)
* Inline equations go between a pair of single dollar signs $ — with no space between the signs and the equation itself $E = mc^{2}$
* Block equations go in between a pair of double dollar signs — with or without spaces, it works $$ E = mc^{2}$$
* For inline footnotes, use the ^[footnote] syntax ^[Corresponding author.] the caret sign ^ comes before the left square bracket [this syntax works in YAML as well as in text footnotes in YAML get symbols, in text they get numbers]
* An alternative is to use the [^identifier] syntax, with identifiers defined elsewhere in the same document the caret sign comes after the left square bracket this syntax works in text, but not in YAML
* Lines starting with asterisk * as well as plus + or minus − signs introduce lists
* Lists can be nested within each other, with indentation
* List items can be numbered
* Two hyphens grouped together introduce an en-dash
* Three hyphens grouped together introduce an em-dash
* A pair of tildes introduces subscript CO~2~
* A pair of carets introduces superscript R^2^
* the syntax here (Markdown-based) is different than the one for equations (LaTeX-based) e.g., R^2^ versus mc^{2}

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

## Code Figures Tables




## Meet your instructor

{{< mention "admin" >}}

## FAQs

{{< spoiler text="Are there prerequisites?" >}}
There are no prerequisites for the first course.
{{< /spoiler >}}

{{< spoiler text="How often do the courses run?" >}}
Continuously, at your own pace.
{{< /spoiler >}}

{{< cta cta_text="Begin the course" cta_link="Import" >}}


