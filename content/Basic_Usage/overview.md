# Overview

In this section, we would like to introduce basic functions of `SnpHub`.

When you open `Snphub` in browser, you would see the page like the picture below.

![Overview of SnpHub](./../img/overview-1.jpg)

Basically, we can devide the whole page into two parts:
- ①: *Tag*s. By clicking them, you could change from different functions.
- ②: *Content*. This is the main panel where you actually use the application.

In the *content* part of the page, you may found the input panal on the left, in most of the functions. Some of the inputs are similar.

## Common input boxes

When the textbox has a title called "**Samples**", **sample names** are wanted here. Three ways are avaliable to input:
- Pure sample name list. Sample names are divided by *,*, like `sample1,sample2,sample3`.
- Pure group list. Use a *#* before group name to transfer group into sample name list, like `#pre-defined-group-name-1,#pre-defined-group-name-2`. 
- Mixed list. Something looks like `sample1,sample2,sample3,#pre-defined-group-name-1`

![Mixed use of sample and group in sample input](./../img/overview-2.jpg)

When the textbox has a title of "**Groups**, **groups** are needed here. Three ways are avaliable as well.
- Pure sample name group list. Assume that we have samples `S1,S2,S3,S4`, and `S1,S2` are in a group called `G1`, while `S3,S4` in `G2`, a string like `G1{S1,S2},G2{S3,S4}` could be used as an input.
- Pure group list. Assume that we have two pre-defined groups called `PG1` and `PG2`, a string like `PG1,PG2` could be used as an input.
- Mixed list. String like `G1{S1,S2},PG1,PG2,G2{S3,S4}` is also able to use as an input.
Make sure that `S1`, `S2`, `S3` and `S4` should **NOT** be contained in neither `PG1` nor `PG2`.

![group input using self-defined group](./../img/overview-3.jpg)

When the textbox has a title of "**Region**, a region is wanted here. Input format should be `chr:from-to`, like `chr1A:1-100`. You could find the avaliable chromsomes and their length in `SampleInfo` tag. Also, gene name is acceptable.

![region input](./../img/overview-4.jpg)

We will show more details later.