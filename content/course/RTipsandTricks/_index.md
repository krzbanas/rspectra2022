---
title: 📊 Some tips and tricks
linkTitle: Tips
summary: Tips and tricks
date: '2021-01-24'
weight: 60
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


## Use `here` package

```r
library(here)

# specify full path to the data files
data01<-here::here("FOLDER","SUBFOLDER", "file01.csv")
# call the function
dataset01 <- read_csv(data01)
# this code chunk is OS universal
```

`here::here()` figures out the top-level of the current project using some sane heuristics. It looks at working directory, checks a criterion and, if not satisfied, moves up to parent directory and checks again. Lather, rinse, repeat.

Here are the criteria. The order doesn’t really matter because all of them are checked for each directory before moving up to the parent directory:

- Is a file named .here present?
- Is this an RStudio Project? Literally, can I find a file named something like foo.Rproj?
- Is this an R package? Does it have a DESCRIPTION file?
- Is this a remake project? Does it have a file named remake.yml?
- Is this a projectile project? Does it have a file named .projectile?
- Is this a checkout from a version control system? Does it have a directory named .git or .svn? Currently, only Git and Subversion are supported.

If no criteria match, the current working directory will be used as fallback. Use `set_here()` to create an empty .here file that will stop the search if none of the other criteria apply. `dr_here()` will attempt to explain why here decided the root location the way it did. See the function reference for more detail.

## Problem with the function name

Sometimes the same function name is used in various libraries, so the order of the libraries loading matters as latter library will *mask* the function with it's own definition.
This may cause the problems in the code if the User calls the function and is expecting different behaviour. There are two ways to deal with this issue. One is to rename the function in question before loading next package that contains the function under the same name. Another (recommended) is to write in code explictly function from which package should be used To specify the package that you want to use, the syntax is following 'package::function.name()'  


```r
chron::is.weekend()
tseries::is.weekend()

#In other words, use 
package.name::function.name()
#In addition, if you know that you will always want to use the function in chron, #you can define your own function as follows:
is.weekend <- chron::is.weekend #EDIT

library(chron)
is.weekend.chron <- is.weekend
library(tseries)
# then you can call is.weekend for the tseries version or is.weekend.chron for the chron version


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


