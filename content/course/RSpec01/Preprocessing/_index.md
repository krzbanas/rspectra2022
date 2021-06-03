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

## Bining 

## Range Cutting

## Baseline correction

### Asymmetric Least Squares
Baseline correction by 2nd derivative constrained weighted regression.
### Fill peaks
An iterative algorithm using suppression of baseline by means in local windows
### Iterative Restricted Least Squares
An algorithm with primary smoothing and repeated baseline suppressions and regressions with 2nd derivative constraint.
### Low-pass FFT filter
An algorithm for removing baselines based on Fast Fourier Transform filtering
### Median window
An algorithm finding medians in local windows and smoothing with gaussian weighting
### Modified polynomial fitting
Polynomial fitting with baseline suppression relative to original spectrum
### Simultaneous Peak Detection and Baseline Correction
Peak detection is done in several steps sorting out real peaks through different criteria.  Peaks areremoved from spectra and minimums and medians are used to smooth the remaining parts of thespectra. Ifsnminimumis omitted, y3, midspec, y and y2 are not returned (faster)
### Robust Baseline Estimation
algorithm based on LOWESS and weighted regression
### Rolling ball
Ideas from Rolling Ball algorithm for X-ray spectra by M.A.Kneen and H.J. Annegarn.  Variablewindow width has been left out
### Shirley Background Estimation

## Normalization
 
 ### Min-Max (zero2one)
 
 ### Area (TotInt)
 
 ### Band (Range)
 
 ### Probabalistic Quotient Normalization
 
 

## Quiz

{{< spoiler text="What is PQN?" >}}
Probabalistic Quotient Normalization
{{< /spoiler >}}

