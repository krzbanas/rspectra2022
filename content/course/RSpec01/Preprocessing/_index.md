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
Shirley Background correction for X-ray Photoelectron Spectroscopy.
The shape of the spectrum background or baseline is affected by inelastic energy loss processes,secondary electrons and nearby peaks. A reasonable approximation is essential for a qualitative andquantitative analysis of XPS data especially if several components interfere in one spectrum.  The choice of an adequate background model is determined by the physical and chemical conditions of the measurements and the significance of the background to the information to be obtained.  The subtraction of the baseline before entering the fit iterations or the calculation of the peak area can be an acceptable approximation for simple analytical problems. In order to obtain chemical and physical parameters in detail, however, it is absolutely necessary to include the background function in the iterative peak fit procedure.
### TAP
An implementation of Roman Svoboda and Jirí Málek’s algorithm for baseline identification inkinetic anlaysis of derivative kinetic data.
1. A first approximation of the baseline equation is selected as the straight line between start andend of the curve. 
2. Based on the first approximation of the baseline equation, the phase changeprogress parameter is calculated.  
3. An updated equation of the baseline is calculated and thephase change progress parameter equation from step 2. 
4. The baseline equation from step 3 is compared (point by point) with the one from the previous iteration. If the convergence criterion is met (the difference between every baseline value corresponding to two successive iterations was less than 0.1%) the procedure is stopped and the final baseline equation is selected.  If the convergence criterion  is  not  fulfilled  then  a  new  iteration  is  carried  out  from  step 2 until  convergence was achieved.

## Normalization
 
 ### Min-Max (zero2one)
 
 ### Area (TotInt)
 
 ### Band (Range)
 
 ### Probabalistic Quotient Normalization
 
 

## Quiz

{{< spoiler text="What is PQN?" >}}
Probabalistic Quotient Normalization
{{< /spoiler >}}

