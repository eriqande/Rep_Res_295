README
================
13 April, 2017

-   [General Goals](#general-goals)
-   [Data](#data)
    -   [Reading Data In](#reading-data-in)

<!-- README.md is generated from README.Rmd. Please edit that file -->
General Goals
-------------

This is a simple RStudio project that Kristen Ruegg has put together for the 2017 EEB 295 course with Eric Anderson, "[Case Studies in Reproducible Research](https://eriqande.github.io/rep-res-eeb-2017/)".

The general goals of this project (for our purposes at the moment) are fairly straightforward. We want to learn to import our meta data into Rstudio and interface with Git. It would be amazing if Kristen, Jasmine and Winnie could learn to merge changes and communicate through Git and work and manipulate files in Rstudio.

Data
----

The data for this project are all housed in the `./data` directory. There are two main types of files:

1.  The first file in the data directory is WIFL\_Metadata.csv. This file is the meta data and will be used to help understand and interpret the genetic data files.

2.  The second file is the SNP data. This is the output from our genotyping efforts. The sample names in the SNP data link to the sample names in the metadata file.

### Reading Data In

#### Metadata files

The Metadata files can be read in like this (one can also get hints about code needed to read in the data by clicking on the file in the data folder. That being said, eric says you have to be careful to change the path name to the current working directory which is ./data):

``` r
library(readr)
WIFL_Metadata <- read_csv("./data/WIFL_Metadata.csv")
#> Parsed with column specification:
#> cols(
#>   Field_Number = col_character(),
#>   `SNP Plate Number` = col_integer(),
#>   `SNP Well Position` = col_character(),
#>   Near_Town = col_character(),
#>   Extraction_Location = col_character(),
#>   Collector = col_character(),
#>   Country = col_character(),
#>   State = col_character(),
#>   Lat = col_double(),
#>   Long = col_double(),
#>   Group = col_character(),
#>   Stage = col_character(),
#>   `Stage (notes)` = col_character(),
#>   Year = col_integer(),
#>   Month = col_integer(),
#>   Day = col_integer(),
#>   `RAD?` = col_character()
#> )
```
