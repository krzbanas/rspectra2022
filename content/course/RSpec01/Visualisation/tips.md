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

add chip transition lines:

```r
p5<-p4+geom_vline(xintercept=c(1689,1456,1203),
                  colour="blue", alpha=0.9)
```
... and dashed lines:

```r
p6<-p5+geom_vline(xintercept=c(1144,1387,1481,1724), 
                  colour="red", linetype = "dashed", alpha=0.5)
```
### Rectangles

### Labels
add optimization lines labels:
```r
op_lines<- data.frame(c(1144,1387,1481,1724))
colnames(op_lines)<-"Position"
p7<-p6+geom_label_repel(data=op_lines,
                        aes(x=Position, y=0.25, label=Position), colour="red")
```
