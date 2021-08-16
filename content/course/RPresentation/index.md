---
title: R Presentation
linkTitle: RPresentation
summary: R Presentation
date: '2021-07-12'
weight: 70
type: book
---


## What you will learn

Basics of R Markdown for presentation preparation in R. 

## Courses in this program

{{< list_children >}}

R Markdown for preparing the presentations : xaringan package

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


## Links, footnotes, equations, lists

- internal links: add `name: contents-slide` at the beginning of the slide, refer by `Go [back to Contents](#contents-slide)`
- this strategy can work in both directions—not only for linking backwards, but also forwards in a presentation.


## Own title page

- In YAML set seal: false
- Then create title slide from scratch: 
```r
 ---
class: inverse, center, middle
background-image: url(figs/p_and_p_cover.png)
background-size: cover
# Text Mining
<img src="figs/blue_jane.png" width="150px"/>
### USING TIDY PRINCIPLES
.large[Julia Silge | Deming Conference | 4 Dec 2018]
```

## Built-in themes
- `output:
  xaringan::moon_reader:
    css: [default, metropolis, metropolis-fonts]`
- available options: (2*14)  "chocolate-fonts" "chocolate" "default-fonts"  "default"  "duke-blue"  "hygge-duke"   "hygge"   "kunoichi"  "lucy-fonts"  "lucy"  "metropolis-fonts" "metropolis"  "middlebury-fonts" "middlebury"  "ninjutsu" "rladies-fonts"    "rladies"   "robot-fonts"      "robot"            "rutgers-fonts"    "rutgers"          "shinobi"          "tamu-fonts"       "tamu"             "uo-fonts"    "uo"     "uol-fonts"       
 "uol"


## References


## Code

-  Code highlighting:  wrapping a line in the code with ``{{..code..}}``, that line will be highlighted in the slides
-  Another option: comment from the right `#<<` 
-  Do not forget to set highlight in YAML
  `output: 
  xaringan::moon_reader:
    nature:
      highlightStyle: github
      highlightLines: true`
-  Available highlight styles are: arta, ascetic, dark, default, far, github, googlecode, idea, ir-black, magula, monokai, rainbow, solarized-dark, solarized-light, sunburst, tomorrow, tomorrow-night-blue, tomorrow-night-bright, tomorrow-night, tomorrow-night-eighties, vs, zenburn

## Tables
  - basic `head(tx_names)`
  - kable `head(tx_names) %>% knitr::kable(format = "html") `
  - DT    `library(DT) head(tx_names) %>% datatable()`
  - gt    `library(gt) head(tx_names) %>% gt()`
      
## Background image, logo, other images
-  Add image
      - `![](img/camera-green.jpg)` (markdown)
      - `knitr::include_graphics("img/camera-green.jpg")` (knitr)
      - `<img src="img/camera-green.jpg" width="90%" align="right"/>` (html)
      -  try to keep your images in subdirectory (called img or figures or whattoyoulike) with respect to presentation.Rmd file
      -  Maps: `library(leaflet) leaflet() %>% addTiles() %>% setView(lat = 30.2621, lng = -97.7382, zoom = 17)` 

## Icons
- `r emo::ji("smile") (surrounded by backticks)`
- Copy and paste html directly from the website: `<i class="fas fa-brain"></i>`
- use `icon::fa("rocket")` bigger `icon::fa("rocket", size = 2)` animated `icon::fa("rocket", size = 5, animate = "spin")`
- use `r icons::fontawesome("brain")`


## Presentation mode (shortcuts)

-  key `h` (Help) or `?` on your keyboard to learn all possible keyboard shortcuts, which may help you better present your slides, press `h` or `?` again to exit the help page.
-  To go the previous slide, you may press `Up/Left` arrows, `PageUp`, or `k`
-  To go the next slide, you may press `Right/Down` arrows, `PageDown`, `Space`, or `j`
-  `Home` to go to the first slide, or `End` to go to the last slide
-  Typing a number and pressing `Return` (or `Enter`), you can jump to a specific slide with that page number
-  `b` to black out a slide, and `m` to “mirror” a slide (reverse everything on the slide). These techniques can be useful when you do not want the audience to read the slide, e.g., when you have solutions on a slide but do not want to show them to your students immediately. I encourage you to try `m`; it can be a lot of fun. You can press these keys again to resume the normal slide
-  `f` to toggle the fullscreen mode
-  `c` to clone the slides to a new browser window; slides in the two windows will be in sync as you navigate through them
-  `p` to toggle the presenter mode. The presenter mode shows thumbnails of the current slide and the next slide on the left, presenter notes on the right, and also a timer on the top right. The keys c and p can be very useful when you present with your own computer connected to a second screen (such as a projector). On the second screen, you can show the normal slides, while cloning the slides to your own computer screen and using the presenter mode. Only you can see the presenter mode, which means only you can see presenter notes and the time, and preview the next slide. You may press `t` to restart the timer at any time
-  `o` for overview (with xaringanExtra: Tile View option)
-  `w` to turn the webcam on and off (with xaringanExtra: Webcam option)
-  `s` to turn drawing mode on and off (with xaringanExtra: Scribble)
    



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



