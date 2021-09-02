---
title: Graphics Tips
linkTitle: Tips
date: '2021-01-01'
type: book
weight: 80
math: true
tags:

---

Graphics Tips

## Annotations
There is a number of things you may want to add to your plot: lines, semi-transparent areas, text labels etc. The most flexible and easiest way to do this is within ggplot2 graphics system, so I focus on this topic.

### Lines
Often we would like to add solid or dashed line marking the position of the band (peak).
```r
## add chip transition lines
p5<-p4+geom_vline(xintercept=c(1689,1456,1203), colour="blue", alpha=0.9)
```
### Rectangles

### Labels


