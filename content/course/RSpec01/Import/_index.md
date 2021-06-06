---
title: Import data
linkTitle: Import
date: '2021-01-01'
type: book
weight: 40
math: true
tags:
  - Statistics
---

How to import spectral data into R.

<!--more-->

{{< icon name="clock" pack="fas" >}} 1-2 hours per week, for 8 weeks

## In ChemoSpec

```r
library(ChemoSpec)

# create SpectraObject
spectra01<-matrix2SpectraObject(gr.crit = c("Control","Infected"),
                                gr.cols = c("auto"),
                                freq.unit = "Wavenumber [cm -1]",
                                int.unit = "Absorbance [a.u.]",
                                descrip = "Aspirin Study",
                                in.file = "spectra01.csv",
                                out.file = "spectra01",
                                chk = TRUE,
                                sep = ",",
                                dec = ".")
# check
sumSpectra(spectra01)
```

{{< callout note >}}
The parameter $\mu$ is the mean or expectation of the distribution.
$\sigma$ is its standard deviation.
The variance of the distribution is $\sigma^{2}$.
{{< /callout >}}

## Quiz

{{< spoiler text="What is the parameter $\mu$?" >}}
The parameter $\mu$ is the mean or expectation of the distribution.
{{< /spoiler >}}

