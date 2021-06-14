---
title: Pre-processing of spectra
linkTitle: Preprocessing
date: '2021-01-01'
type: book
weight: 20
math: true
tags:
  - Statistics
---

Spectral preprocessing

<!--more-->

{{< icon name="clock" pack="fas" >}} 1-2 hours per week, for 8 weeks



## Smoothing

```r
all02 <- spc.loess (all01 , seq (400, 4000, 1))
all02 <- spc.loess (all01 , seq (400, 4000,  length.out = 1000))
```


## Bining 

## Range Cutting

