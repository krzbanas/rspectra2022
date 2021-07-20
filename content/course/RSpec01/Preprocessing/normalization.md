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
 
 ```r
 # in hyperSpec
 hyper02<-sweep(hyper01, 1, mean, "/")
 # in ChemoSpec
 spectra01n_area<-normSpectra(spectra01, method="TotInt")
 ```
 
 ### Band (Range)
 
 ### Probabalistic Quotient Normalization
 
  ```r

 # in ChemoSpec
 spectra01n_PQN<-normSpectra(spectra01, method="PQN")
 ```

### Another normalization
If there is a requirement for using another normalization factor (for example to beam current value for XRF spectra) we can use similar approach as presented in Area section.

 ```r
#calculate normalization factor (divide by beam current and multiply by 1000 - for convenience)
norm01<-1000/df$BC
#then `sweep` over all spectra (remember that in hyperSpec object spectra are in rows so we should declare 1 as the margin)
spectra01n<-sweep(spectra01,1,norm01,"*")
 ```



## Quiz

{{< spoiler text="What is PQN?" >}}
Probabalistic Quotient Normalization
{{< /spoiler >}}


