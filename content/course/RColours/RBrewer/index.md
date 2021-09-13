---
title: 📊 Colours in R
linkTitle: Colours in R
summary: Colours in R
date: '2021-01-24'
weight: 10
type: book
---



## `RColorBrewer`

```r
library("RColorBrewer")
display.brewer.all()
```
- Sequential palettes (first list of colors), which are suited to ordered data that progress from low to high (gradient). The palettes names are : Blues, BuGn, BuPu, GnBu, Greens, Greys, Oranges, OrRd, PuBu, PuBuGn, PuRd, Purples, RdPu, Reds, YlGn, YlGnBu YlOrBr, YlOrRd.
- Qualitative palettes (second list of colors), which are best suited to represent nominal or categorical data. They not imply magnitude differences between groups. The palettes names are : Accent, Dark2, Paired, Pastel1, Pastel2, Set1, Set2, Set3.
- Diverging palettes (third list of colors), which put equal emphasis on mid-range critical values and extremes at both ends of the data range. The diverging palettes are : BrBG, PiYG, PRGn, PuOr, RdBu, RdGy, RdYlBu, RdYlGn, Spectral

Blues Greens Greys Oranges Purples Reds

## Palettes in `ggplot2`

```r
scale_colour_brewer(..., type = "seq", palette = 1, direction = 1)
scale_fill_brewer(..., type = "seq", palette = 1, direction = 1)
scale_colour_distiller(..., type = "seq", palette = 1, direction = -1,
  values = NULL, space = "Lab", na.value = "grey50",
  guide = "colourbar")
scale_fill_distiller(..., type = "seq", palette = 1, direction = -1,
  values = NULL, space = "Lab", na.value = "grey50",
  guide = "colourbar”)
d + scale_colour_brewer(palette = "Greens”)
p + scale_fill_brewer(direction = -1)
```

## `paletteer` package

This a one stop destination for anyone looking for a color palette to use in `r`.
Following packages are included:
 - `awtools`
 - `cartography`
 - `dichromat`
 - `dutchmasters`
 - `ggsci`
 - `ggpomological`
 - `ggthemes`
 - `ghibli`
 - `grDevices`
 - `jcolors`
 - `LaCroixColoR`
 - `NineteenEightyR`
 - `nord`
 - `ochRe`
 - `oompaBase`
 - `palettetown`
 - `palr`
 - `pals`
 - `Polychrome`

##  Colour-blind friendly palettes

## Other resources to work with colours (not `R` or partially `R` related)

 - [Color Universal Design (CUD) - How to make figures and presentations that are friendly to Colorblind people](https://jfly.uni-koeln.de/color/)

