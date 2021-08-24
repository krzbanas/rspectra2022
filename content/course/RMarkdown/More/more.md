---
title: Links, footnotes, equations, lists
linkTitle: More
summary: Links, footnotes, equations, lists
date: '2021-01-24'
weight: 20
type: book
---


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


