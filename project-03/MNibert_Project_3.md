---
title: "Visualizing Text and Distributions"
output: 
  html_document:
    keep_md: true
    toc: true
    toc_float: true
---

# Data Visualization Project 03

## Part 1: Density Plots

Using the dataset obtained from FSU's [Florida Climate Center](https://climatecenter.fsu.edu/climate-data-access-tools/downloadable-data), for a station at Tampa International Airport (TPA) from 2016 to 2017, attempt to recreate the charts shown below


```r
library(tidyverse)
library(lubridate)
library(ggridges)

weather_tpa <- read_csv("https://github.com/reisanar/datasets/raw/master/tpa_weather_16_17.csv")

weather_tpa <- weather_tpa %>% 
  mutate(data_date = make_date(year, month, day)) %>% 
  mutate(data_month = month(data_date, label = TRUE, abbr = FALSE))

weather_tpa
```

```
## # A tibble: 367 x 8
##     year month   day precipitation max_temp min_temp data_date  data_month
##    <dbl> <dbl> <dbl>         <dbl>    <dbl>    <dbl> <date>     <ord>     
##  1  2016     1     1          0          81       70 2016-01-01 January   
##  2  2016     1     2          0          73       59 2016-01-02 January   
##  3  2016     1     3          0.18       61       50 2016-01-03 January   
##  4  2016     1     4          0          66       49 2016-01-04 January   
##  5  2016     1     5          0          68       49 2016-01-05 January   
##  6  2016     1     6          0          67       54 2016-01-06 January   
##  7  2016     1     7          0          72       56 2016-01-07 January   
##  8  2016     1     8          0.54       76       63 2016-01-08 January   
##  9  2016     1     9          0.65       78       62 2016-01-09 January   
## 10  2016     1    10          0          72       56 2016-01-10 January   
## # ... with 357 more rows
```

### Plot 1

There is some different design choices in mine versus the one in the project outline. I like the gridlines here more because with each month on it's own graph, it makes it easier for me to view. The gray background also makes it look more modern in my eyes. 

```r
ggplot(weather_tpa, 
       aes(x = max_temp,
           fill = data_month)) +
  geom_histogram(binwidth = 3) +
  guides(fill = FALSE) +
  facet_wrap(~ data_month) +
  labs(x = "Maximum Temperatures", y = "Number of Days")
```

![](MNibert_Project_3_files/figure-html/unnamed-chunk-2-1.png)<!-- -->


But if I were to go for complete copy:


```r
ggplot(weather_tpa, 
       aes(x = max_temp,
           fill = data_month)) +
  geom_histogram(binwidth = 3) +
  guides(fill = FALSE) +
  facet_wrap(~ data_month) +
  theme_bw() +
  theme(panel.grid.major = element_blank(), 
        panel.grid.minor = element_blank(),
        panel.background = element_blank()) +
  labs(x = "Maximum Temperatures", y = "Number of Days")
```

![](MNibert_Project_3_files/figure-html/unnamed-chunk-3-1.png)<!-- -->


### Plot 2

```r
ggplot(weather_tpa, 
       aes(x = max_temp)) +
  geom_density(bw = 0.5, color = "black", fill = "grey") +
  scale_fill_grey() +
  theme(panel.grid.major = element_blank(), 
        panel.grid.minor = element_blank(),
        panel.background = element_blank()) +
  labs(x = "Maximum Temperature", y = "Density")
```

![](MNibert_Project_3_files/figure-html/unnamed-chunk-4-1.png)<!-- -->


### Plot 3

```r
ggplot(weather_tpa, 
       aes(x = max_temp,
           fill = data_month)) +
  geom_density() +
  guides(fill = FALSE) +
  facet_wrap(~ data_month) +
  theme_bw() +
  theme(panel.grid.major = element_blank(), 
        panel.grid.minor = element_blank()) +
  labs(x = "Maximum Temperatures", y = "")
```

![](MNibert_Project_3_files/figure-html/unnamed-chunk-5-1.png)<!-- -->


### Plot 4

```r
ggplot(weather_tpa, aes(x = max_temp, y = data_month,
                               fill = data_month)) +
  geom_density_ridges(scale = 2, quantile_lines = TRUE, quantiles=2) +
  guides(fill = FALSE) +
  labs(x = "Maximum Temperature", y = NULL) +
  theme_minimal()
```

```
## Picking joint bandwidth of 1.49
```

![](MNibert_Project_3_files/figure-html/unnamed-chunk-6-1.png)<!-- -->


### Plot 5

```r
ggplot(weather_tpa, aes(x = max_temp, y = data_month,
                               fill = ..x..)) +
  geom_density_ridges_gradient(quantile_lines = TRUE, quantiles=2) +
  scale_fill_viridis_c(option = "plasma", name ="") +
  labs(x = "Maximum Temperature (in degrees Fahrenheit)", y = NULL) +
  theme_minimal()
```

```
## Picking joint bandwidth of 1.49
```

![](MNibert_Project_3_files/figure-html/unnamed-chunk-7-1.png)<!-- -->

