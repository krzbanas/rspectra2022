---
title: Import data
linkTitle: One Column
date: '2021-06-09'
type: book
weight: 20
math: true
tags:
  - Statistics
---

# How to import spectral data into R?

## Folder with one column ASCII files

Each spectrum is in separate text file (ASCII) with one column:  intensity (absorbance, transmitance etc.)
Energy related vector (x-axis) is provided in separate file.

### In ChemoSpec

```r
library(ChemoSpec)

```


{{< callout note >}}
If the data files are in different folder (or subfolder) one should provide `path`. Both full path and relative (`r path ="DATA"`) work.
{{< /callout >}}


### In hyperSpec

```r
library(hyperSpec)

```


## Quiz

{{< spoiler text="What function to use in R to transpose matrix?" >}}
Function name is  `t(matrix)`
{{< /spoiler >}}

