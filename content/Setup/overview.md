# Overview

In this section, we will introduce how to setup our NGBT application. Some basic knowledge about linux, R and resequencing is required. Also, you need to have a server with **shiny server** installed. If not, see [here](https://www.rstudio.com/products/shiny/download-server/).

Further more, there are several R packages need to be installed, which are `crayon`, `RColorBrewer`, `ggplot2`, `ggtree`, `pegas`, `vcfR`, `ape` and `DT`. If any of them does not exist in the server, NGBT may not work. However, this error will be detected by the `check.R`, which is a setup **checking** script that is supposed to be executed **every time configuration file changed**.

## Check your config

Each time you set/changed your configuration, use:
``` shell
./install.sh
```
to get the new data file processed and checked.