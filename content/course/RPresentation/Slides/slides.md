---
title: Slides
linkTitle: Slides
summary: Slides
date: '2021-07-12'
weight: 10
type: book
---

## Slides

- Every new slide is created under three dashes (`---`). 
- A slide can have a few properties, including class and background-image, etc. Properties are written in the beginning of a slide
- Background images can be set via the background-image property. The path should be put inside url()
- There is a special slide, the title slide, that is automatically generated from the YAML metadata of your Rmd document
- You can also disable the automatic title slide via the seal option and create one manually by yourself
- Slides content may be align with declaration `class: center, middle` (options are: left center right and top middle bottom)
- Align some text only with `.right[text]` (options are: left center right)


## Content Classes

- The default theme of xaringan has provided four more content classes:
- `.left-column[ ]` and `.right-column[ ]` provide a sidebar layout. The left sidebar is narrow (20% of the slide width), and the right column is the main column (75% of the slide width). If you have multiple level-2 (##) or level-3 (###) headings in the left column, the last heading will be highlighted, with previous headings being grayed out.
- `.pull-left[ ]` and `.pull-right[ ]` provide a two-column layout, and the two columns are of the same width.

## Incremental Slides

- to show content incrementally on a slide (e.g., holding a funny picture until the last moment), you can use two dashes to separate the content.
- The two dashes can appear anywhere except inside content classes, so you can basically split your content in any way you like
- There are a few other advanced ways to build incremental slides documented in the presentation [here](https://slides.yihui.name/xaringan/incremental.html)


## Presenter Notes

- You can write notes for yourself to read in the presenter mode (press the keyboard shortcut p). These notes are written under three question marks `???` after a slide, and the syntax is also Markdown, which means you can write any elements supported by Markdown, such as paragraphs, lists, images, and so on
- Slides are not papers or books, so you should try to be brief in the visual content of slides, but verbose in verbal narratives.

