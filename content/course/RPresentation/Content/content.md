---
title: Content
linkTitle: Content
summary: Content
date: '2021-07-12'
weight: 40
type: book
---

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


## Links, footnotes, equations, lists

- internal links: add `name: contents-slide` at the beginning of the slide, refer by `Go [back to Contents](#contents-slide)`
- this strategy can work in both directions—not only for linking backwards, but also forwards in a presentation.


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
- use academicons `r icons::fontawesome("orcid")`

## References

