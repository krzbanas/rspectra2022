---
title: 📊 Graphics Tips
linkTitle: Graphics
summary: Tips and tricks
date: '2021-08-17'
weight: 70
type: book
---

# Repel Labels

## Use `ggrepel` package

```r
library(ggrepel)

# specify full path to the data files
data01<-here::here("FOLDER","SUBFOLDER", "file01.csv")
# call the function
dataset01 <- read_csv(data01)
# this code chunk is OS universal
```

# Plotly
## Testing
```r
library("plotly")
p1<-plot_ly(economics, x = ~ date, y = ~ unemploy / pop)
p1
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

