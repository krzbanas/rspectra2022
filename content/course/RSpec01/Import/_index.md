---
title: Import data
linkTitle: Import
date: '2021-01-01'
type: book
weight: 10
math: true
tags:
  - Statistics
---

How to import spectral data into R?

<!--more-->

## Matrix

### In ChemoSpec

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
The parameter $gr.crit$ is used for dividing the spectra into groups.
{{< /callout >}}



### In hyperSpec

```r
library(hyperSpec)
# import data
dataset01 <- read.csv("spectra01.csv")
# first column - wavenumbers (must be vector)
wavenumber<-as.vector(dataset01[,1])
# second to last column - 
# spectra matrix (must be transposed: subsequent spectra in rows)
spectra<-t(as.matrix(dataset01[,-1]))
# extra data slot - extract column names (must be data.frame)
d1<-data.frame(colnames(dataset01[,-1]))
colnames(d1)<-c("names")
#make hyperSpec object
object01<-new("hyperSpec", wavelength = wavenumber,
              spc = spectra, data=d1)
#check
object01
```
## Matrix

### In ChemoSpec

```r
library(ChemoSpec)
# create SpectraObject
spec <- files2SpectraObject(gr.crit = c("T01","T02","T03","T04"),
                            gr.cols = c("auto"),
                            freq.unit = "Wavenumber [cm -1]",
                            int.unit = "Absorbance [a.u.]",
                            descrip = "Propolis",
                            path ="D:/CHEMOSPEC_PCA_TEST/DATA/",
                            fileExt = "\\.(txt|TXT)$",
                            out.file = "spectra02",
                            chk = TRUE,
                            sep = ",",
                            dec = ".")
# check
sumSpectra(spectra01)
```


{{< callout note >}}
If the data files are in different folder (or subfolder) one should provide $path$
{{< /callout >}}



## Quiz

{{< spoiler text="What function to use in R to transpose matrix?" >}}
Function $t(matrix)$
{{< /spoiler >}}

