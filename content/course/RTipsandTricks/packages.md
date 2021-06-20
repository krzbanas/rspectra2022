---
title: 📊 PAckages
linkTitle: Tips
summary: Tips and tricks
date: '2021-01-24'
weight: 20
type: book
---


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


