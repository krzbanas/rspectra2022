---
title: Import data
linkTitle: Import
date: '2021-06-09'
type: book
weight: 40
math: true
tags:
  - Statistics
---

# How to import spectral data into R?

## HDF5

```r
install.packages("BiocManager")
BiocManager::install("rhdf5")
library(rhdf5)
h5f01 = H5Fopen("DATA/CobayeOne_FTIR.hdf5")
h5f01
```

