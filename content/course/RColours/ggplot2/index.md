---
title: 📊 Colours in ggplot2 
linkTitle: Colours in ggplot2 
summary: Colours in ggplot2 
date: '2021-01-24'
weight: 20
type: book
---



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
