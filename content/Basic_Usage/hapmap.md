# HapMap

Haplotype map provide a clear way to see the relationship between haplotype and realworld location. It's like to draw a haplotype network, groupping by the location of the samples instead of the genetic distance. It will be useful when you want to see the regional difference.

![HapMap tag](./../img/HapMap-2.jpg)

## Panel ① on the left provides severial options:
- **Samples**: sample names are wanted here. For example, you could input `sample1,sample2,sample3`. Also, if a sample group has been defined by the administrator, which you could see in the `SampleInfo` panel, and all samples in a particular group are needed, you could use `#pre-defined-group-name-1` to add all of the samples in the group pre-defined-group-name1. **NOTE** that a hash mark is needed because the input shoud be **samples** rather than **groups**.

- **Site**: a **SINGLE site** is wanted here. Input format should be `chr:pos`, like `chr1A:123`. You could find the avaliable chromsomes and their length in `SampleInfo` panel. 

- **Longitude range**: decide the maximun and minimum of the longitude to draw on the plot.

- **Latitude range**: decide the maximun and minimum of the latitude  to draw on the plot.

- **Diatance merge range**: coefficient of the merge range. Larger the coefficient is, bigger the merge range is. And merge range means the pies on he plot may be merged into one, because they are too close (in the merge range).

- **Draw**: click after fulfill options, and panel ② will display the plot (if every settings are correct).

## Download Options

Click the **Download Options** button, and then you can select the format, the width, the height of the file you download. Then, click `Download` to download the plot.
