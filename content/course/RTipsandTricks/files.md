---
title: 📊 Files Manipulation
linkTitle: Files
summary: Tips and tricks
date: '2021-05-24'
weight: 50
type: book
---


## Save multiple files with automatic naming

```r
#
# export every spectrum to single file (automaticaly named) in long format 
# two columns with many rows - first column wavenumber second column absorbance no headers
# if hyperSpec object test have more than 10 spectra first 10 will be exported with this code
#
for(i in 1:10)
{ 
  name = paste(i,".","csv", sep = "")
  write.txt.long(test[i,,],file=name, cols = c(".wavelength","spc"),col.names =FALSE)
}
```


## Meet your instructor

{{< mention "admin" >}}

## FAQs

{{< spoiler text="Are there prerequisites?" >}}
There are no prerequisites for the first course.
{{< /spoiler >}}

{{< spoiler text="How often do the courses run?" >}}
Continuously, at your own pace.
{{< /spoiler >}}

{{< cta cta_text="Begin the course" cta_link="Tips" >}}
