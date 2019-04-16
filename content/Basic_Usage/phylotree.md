# PhyloTree

![PhyloTree tag](./../img/PhyloTree-1.jpg)

There're two main founction in this tag, which are NJ-tree and MDS (multidimensional scaling). The former, clearly, is the [phylogenetic tree](https://en.wikipedia.org/wiki/Phylogenetic_tree) made by [neighbor joining](https://en.wikipedia.org/wiki/Neighbor_joining) algorithm. And the latter is multidimensional scaling, which present the relationship in the second dimension by the distance on the graph.

![MDS of PhyloTree tag](./../img/PhyloTree-2.jpg)

## Panel ① on the left provides severial options:
- **Type**: choose to draw a phylogenetic tree or a multidimensional scaling plot.

- **Tree layout**: if you choose `NJ-tree` as the plot type, this option would appear. Select a tree layout here.

- **Real branch length**: real branch length means the length of branch present exactly how far the sample from each other. However, some times the real distance between samples is not that importent, and you just want to see the relationship or just want to make a beautiful plot, in this situation, just click `No`. 

- **Groups**: samples that divided into group(s) are wanted. You can define your own group here, by inputing `self-group-name-1{sample1,sample2},self-group-name-2{sample3}`, which means we inputed two groups whose names are "self-group-name-1" and "self-group-name-2". Self-group-name-1 contains sample1 and sample2, while self-group-name-2 contains sample3. You can also use pre-defined groups, by inputing `pre-defined-group-name-1,pre-defined-group-name-2`. **Note** that you could use only **one** type of them, self-defined group or pre-defined group. **Make sure** that the samples in total should **NOT** less than 3, or the tree couldn't be built.

- **Region**: a region is wanted here. Input format should be `chr:from-to`, like `chr1A:1-100`. You could find the avaliable chromsomes and their length in `SampleInfo` panel. Also, gene name is acceptable.

- **Flanking region length**: when you want to use the gene name as region, you may want some extra postions in the upstream or downstream. Value here is simply added to the maximum , and subtracted from the minimum of the region.

- **Draw**: click after fulfill options, and panel ② will display the plot (if every settings are correct).

## Download Options

Click the **Download Options** button, and then you can select the format, the width, the height of the file you download. Then, click `Download` to download the plot.