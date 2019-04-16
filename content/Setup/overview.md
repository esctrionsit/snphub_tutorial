# Overview

In this section, we will introduce how to setup our NGBT application. Some basic knowledge about linux, R and resequencing is required. Also, you need to have a server with **shiny server** installed. If not, see [here](https://www.rstudio.com/products/shiny/download-server/).

## Environment

To run the SnpHub, make sure these softwares are **already** installed:
- samtools
- bcftools
- seqkit
- tabix

Alse, these R packages are also **needed**:
- ggplot2
- ggmap
- dplyr
- rjson
- shiny
- pegas
- vcfR
- ape
- DT


## Check your config

Each time you set/changed your configuration, use:
``` shell
./install.sh
```
to get the new data file processed and checked.