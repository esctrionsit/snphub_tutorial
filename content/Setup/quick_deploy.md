# Overview

> If you don't want to setup the whole environment, we also offer a **Docker-encapsulated version**. For more details, see [here](https://esctrionsit.github.io/snphub_tutorial/content/Docker/overview.html)

In this section, we will introduce how to setup the `SnpHub`. Some basic knowledge about linux, R and resequencing is required. Also, you need to have a server with **shiny server** installed. If not, see [here](https://www.rstudio.com/products/shiny/download-server/).

## Environment

To run the SnpHub, make sure these softwares are **already** installed:
- samtools (no eariler than **v1.4**)
- bcftools (no eariler than **v1.8**)
- seqkit
- tabix (no eariler than **v1.6**)

Also, these R packages are also **needed**:
- ggplot2
- crayon
- ggmap
- dplyr
- rjson
- shiny
- pegas
- maps
- vcfR
- ape
- DT

## Demo

Only two steps are needed to run on demo data set:
- Using command `git clone https://github.com/esctrionsit/snphub` to clone SnpHub to local.
- Using command like `R -e "shiny::runApp('./snphub', port=5000, host='0.0.0.0')"` to run on demo data set. *(Or copy the SnpHub into your `shiny-server app folder`)*

*Make sure that `samtools`, `bcftools`, `seqkit` and `tabix` are added to system PATH. Otherwise, `tool application paths` part in `setup.conf` is needed to change to fit.*

## Setup on own data set

### Fulfill config file

Basic config file is named `setup.conf`, fulfill it and then run command:

``` sh
./setup.R
```

Check [configuration](/content/Setup/configuration.html) for more details about `setup.conf`.

Check [file format](/content/Setup/file-formats.html) for more details about needed files.

If it is your **first time** setting up `SnpHub`, you will also need to delete `advanced_config.R`, and then rename `advanced_config_O.R` to `advanced_config.R`.

### Check your config

Each time you reset/changed your configuration, use:
``` sh
./setup.R
```
to get the new data file pre-processed and checked.