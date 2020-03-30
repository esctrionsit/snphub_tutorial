# HapMap

The **HapMap** function provides a way to project the allele distribution of a single site geographically on a map, utilizing the provided resource-gathering locations.

![HapMap tag](./../img/HapMap-2.jpg)

## Panel ① on the left provides several options:
- **Samples**: sample names are wanted here. Three ways are available to input:
	- Pure sample name list. Sample names are divided by *,*, like `sample1,sample2,sample3`.
	- Pure group list. Use a *#* before group name to transfer group into sample name list, like `#pre-defined-group-name-1,#pre-defined-group-name-2`. 
	- Mixed list. Something looks like `sample1,sample2,sample3,#pre-defined-group-name-1`.

- **Site**: a **SINGLE site** is wanted here.
	- Input format should be `chr:pos`, like `chr1A:123`.
	- If a genomic region is provided, the first variant site in this region will be used for the analysis.

- **Longitude range**: decide the maximum and minimum of the longitude to draw on the plot. A way to cut plot.

- **Latitude range**: decide the maximum and minimum of the latitude  to draw on the plot. Another way to cut plot.

- **Distance merge range**: coefficient of the merge range. Larger the coefficient is, bigger the merge range is. And merge range means the pies on the plot may be merged into one, because they are too close (in the merge range).

- **Draw**: click when getting all options ready.

## Download Options

![Download options](./../img/Download-options-2.gif)

Click the **Download Options** button, and then you can select format, width and height of the plot shown as the result. Then, click `Download` to download it.

## GIF Demonstration

![GIF Demonstration of HapMap](./../img/HapMap-0.gif)