---
title: 📊 Functions
linkTitle: Functions
summary: Tips and tricks
date: '2021-01-24'
weight: 30
type: book
---

## Problem with the function name

Sometimes the same function name is used in various libraries, so the order of the libraries loading matters as latter library will *mask* the function with it's own definition.
This may cause the problems in the code if the User calls the function and is expecting different behaviour. There are two ways to deal with this issue. One is to rename the function in question before loading next package that contains the function under the same name. Another (recommended) is to write in code explictly function from which package should be used To specify the package that you want to use, the syntax is following 'package::function.name()'  


```r
chron::is.weekend()
tseries::is.weekend()

#In other words, use 
package.name::function.name()
#In addition, if you know that you will always want to use the function in chron, 
#you can define your own function as follows:
is.weekend <- chron::is.weekend #EDIT

library(chron)
is.weekend.chron <- is.weekend
library(tseries)
# then you can call is.weekend for the tseries version or is.weekend.chron for the chron version


```

## Custom function output

There are some ways to direct the function output to create an object in the environment. You may modify the body of the function to assign the output to the object (by using `assign` function or `<<-` sign).

```r
import_folder_1C <-function(path, skip, nrows, string) {
  library(hyperSpec)
  files <- list.files (path = path)
  buffer <- read.table(file.path(path,files [1 ]), skip=skip, nrows = nrows)
  spc <- matrix (ncol = nrow (buffer), nrow = length (files))
  spc [1 , ] <- buffer [, 1 ]
    for ( f in seq (along = files)[- 1])
    {
      buffer <- read.table(file.path(path,files [f ]), skip=skip, nrows = nrows)
      spc [f, ] <- buffer[, 1]
    }
  channel <- c(1:nrows)
  sample<-substring(files,1,string)
  df1<-data.frame (sample)
  colnames(df1)=c( "sample")
  spectra01<<-new ("hyperSpec", wavelength = channel, spc = spc, data= df1)
  return(spectra01)
  }
```

Alternatively, you can keep usual `<-` instead of `<<-` command, but with calling the function directly to the new object.

```r
library(here)
data01 <- file.path (here::here("SOLVENT"))
spectra02<-import_folder_1C(data01,19,2048,3)
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

