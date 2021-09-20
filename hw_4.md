**Homework 4**
================

# Calculate the sum of 2 and 3 as follows:

Assign the value 3 to a variable called a. Assign the value 2 to a
variable called b. Print the sum of a and b.

``` r
a <- 3
b <- 2
a + b
```

    ## [1] 5

Calculate the sum of 2 and 3 using the sum() function.

``` r
sum(2, 3)
```

    ## [1] 5

# Flights plotting

Open the flights data frame and make a scatterplot of arrival delay
versus departure delay, for only American Airline flights.

``` r
library(tidyverse)
library(nycflights13)
#glimpse(flights) # Checking var names
AA_flights <- flights %>%
  filter(carrier == "AA")
# glimpse(AA_flights) # Check that it worked
```

Plot departing delays on the x axis and arrival delays on the y axis.

``` r
ggplot(data = AA_flights, mapping = aes(x = dep_delay, y = arr_delay)) +
  geom_point() +
  theme_bw()
```

![](hw_4_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->
