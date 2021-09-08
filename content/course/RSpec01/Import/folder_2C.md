---
title: Import data
linkTitle: Two Columns
date: '2021-06-09'
type: book
weight: 10
math: true
tags:
  - Statistics
---

# How to import spectral data into R?


## Folder with two column ASCII files

Each spectrum is in separate text file (ASCII) with two columns: wavenumber vector in the first column, intensity (absorbance, transmitance etc.) in the second column.

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
If the data files are in different folder (or subfolder) one should provide `path`. Both full path and relative (`r path ="DATA"`) work.
{{< /callout >}}


### In hyperSpec



## Quiz

{{< spoiler text="What function to use in R to transpose matrix?" >}}
Function name is  `t(matrix)`
{{< /spoiler >}}

