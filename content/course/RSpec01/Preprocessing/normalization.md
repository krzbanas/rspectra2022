---
title: Normalization
linkTitle: Normalization
date: '2021-01-01'
type: book
weight: 40
math: true
tags:
  - Statistics
---

## Normalization
 
 ### Min-Max (zero2one)
 
 ### Area (TotInt)
 ```
 # in hyperSpec
 hyper02<-sweep(hyper01, 1, mean, "/")
 # in ChemoSpec
 spectra01n_area<-normSpectra(spectra01, method="TotInt")
 ```
 ### Band (Range)
 
 ### Probabalistic Quotient Normalization
 
 

## Quiz

{{< spoiler text="What is PQN?" >}}
Probabalistic Quotient Normalization
{{< /spoiler >}}


