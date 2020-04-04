# General Setup

> If you don't want to configure the whole environment, we also offer a **Docker-encapsulated version**. For more details, see [here](https://esctrionsit.github.io/snphub_tutorial/content/Docker/overview.html)

In this section, we will introduce how to setup the `SnpHub`. Basic knowledge about Linux, R and resequencing is required. Also, you need to have a server installed with **shiny server**. For more information, please read [here](https://www.rstudio.com/products/shiny/download-server/).

#### Environment

To run the SnpHub, make sure the following software programs are **already** installed:
- samtools (≥ **v1.4**)
- bcftools (≥ **v1.8**)
- seqkit
- tabix (≥ **v1.6**)

Also, the following R packages are also prerequisites:
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

#### Demo

Two steps are needed to run on demo data set:

- Using `git` to clone SnpHub to local.
```sh
git clone https://github.com/esctrionsit/snphub
```

- Using `R` to run on demo data set. *(Or copy the SnpHub into your `shiny-server app folder`)*
```sh
R -e "shiny::runApp('./snphub', port=5000, host='0.0.0.0')"
```

*Make sure that `samtools`, `bcftools`, `seqkit` and `tabix` are added to system PATH. Otherwise, `tool application paths` part in `setup.conf` is needed to change to fit.*

#### Setup with your own data set

##### Fulfill config file

Basic config file is named `setup.conf`, fulfill it and then run command:

``` sh
Rscript ./setup.R
```

Check [configuration](/content/Setup/configuration.html) for more details about `setup.conf`.

Check [file format](/content/Setup/file-formats.html) for more details about required file formats.

If it is your **first time** to set up `SnpHub`, you need to **delete** `advanced_config.R`, and then **rename** `advanced_config_O.R` to `advanced_config.R`.

```sh
rm -f advanced_config.R && mv advanced_config_O.R advanced_config.R
```

##### Check the config file

Each time you reset/changed your configuration, use:
``` sh
Rscript ./setup.R
```
to get the completeness checked and the raw data file pre-processed.