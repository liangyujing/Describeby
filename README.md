```
# Get descriptives
describeBy(manipulation_check, 
           group = picture)

# descriptives
```{r descriptives, include = FALSE}
descriptives <- describeBy(Simulated_Data$Acceptance, 
           group = Simulated_Data$picture)

# Some preliminary descriptives for correct and incorrectly solved trials
describeBy(experimental_df$confidence, group=experimental_df$solution_type,mat=FALSE,type=3)
describeBy(experimental_df$RT, group=experimental_df$solution_type,mat=FALSE,type=3)
describeBy(experimental_df$ACC, group=experimental_df$solution_type,mat=FALSE,type=3)


# read data csv file
library("readr")
my_data <- read.csv(file="R code/antisemitism_07.csv", head=T,sep=";")

## Descriptive statistics for a single group
## Measure of central tendency: mean, median, mode
mean(liedetection)
sd(liedetection)
var(liedetection)
min(liedetection)
max(liedetection)
median(liedetection)
range(liedetection)   #minimum and maximum
summary(liedetection)
quantile(liedetection)

## Graphical display of distributions
library(ggpubr)
#Box plots
ggboxplot(my_data, y = "prejudice", width = 0.5)

library(dplyr)
group_by(my_data) %>% 
  summarise(
    count = n(), 
    mean = mean(prejudice, na.rm = TRUE),
    sd = sd(prejudice, na.rm = TRUE)
  )

## 画图
library("ggpubr")
#Box plot colored by groups: Species
ggboxplot(my_data, x = "liedetection", y = "prejudice",
          color = "liedetection",
          palette = c("#00AFBB", "#E7B800"))

## Frequency tables
table(gender)

```
