Parkrun Results
================

``` r
url_data <- "https://www.parkrun.org.uk/parkrunner/5076650/all/"
```

``` r
read_html('results | parkrun UK.html') %>%
  html_nodes(xpath='//*[@id="results"]') %>%
  html_table() -> Results
  
Results[3]
```

    ## [[1]]
    ## # A tibble: 73 × 7
    ##    Event                 `Run Date` `Run Number`   Pos Time  AgeGrade `PB?`
    ##    <chr>                 <chr>             <int> <int> <chr> <chr>    <chr>
    ##  1 Whinlatter Forest     23/04/2022          141    19 29:34 43.63%   ""   
    ##  2 Lancaster             16/04/2022          254    23 23:32 54.82%   ""   
    ##  3 Lancaster             09/04/2022          253    34 25:08 51.33%   ""   
    ##  4 Severn Valley Country 02/04/2022           72    10 22:55 56.29%   ""   
    ##  5 Erddig                26/03/2022          203     8 21:47 59.22%   ""   
    ##  6 Lancaster             12/03/2022          249    13 22:49 56.54%   ""   
    ##  7 Lancaster             05/03/2022          248    17 22:52 56.41%   ""   
    ##  8 Lancaster             26/02/2022          247    22 22:56 56.25%   ""   
    ##  9 Lancaster             19/02/2022          246    45 25:51 49.90%   ""   
    ## 10 Blackpool             12/02/2022          186    13 22:01 58.59%   ""   
    ## # … with 63 more rows
