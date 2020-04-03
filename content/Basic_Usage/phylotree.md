# PhyloTree, visualize sample distances as a tree

![PhyloTree channel](./../img/PhyloTree-1.jpg)

The **`PhyloTree`** channel supports the exploration of the gene-based genetic distances and evolutionary history based on high-density SNP data. The distance matrix is calculated based on the genetic distances of specified genomic region. Then, two distance-based clustering methods, [neighbor-joining (NJ)](https://en.wikipedia.org/wiki/Neighbor_joining) tree analysis and multidimensional scaling (MDS, also known as PCoA), are supported.

NJ-tree method can rapidly evaluates a large amount of data and is suitable for exploring the genetic relationships among samples for a specific region with a low time cost. Versatile layouts for visualizing the NJ-trees are available, including phylogram, cladogram, unrooted, fan, and radial layouts. Samples in different groups are shown in different colors.

The MDS method supports the visualization of the distances of samples in two-dimensions through non-linear dimensionality reduction. This channel provides users with multiple ways to visualize the sample distances for a specified region.

![MDS of PhyloTree channel](./../img/PhyloTree-2.jpg)

## Panel ① on the left provides several options:
- **Type**: Choose to draw a `phylogenetic tree` or a `multidimensional scaling plot`.

- **Tree layout**: This parameter is only available for drawing `NJ-tree`. Users can select a tree layout here, including `phylogram`, `cladogram`, `fan`, `unrooted` and `radial`.

- **Real branch length**: Specifying `Yes` will present the tree with branch lengths in ratios of the real sample distances. Specifying `No` will present the tree with equal branch lengths.

- **Groups**: The textbox titled "Groups" inquiries a list of group IDs. Both `pre-defined group` and `user-defined group` styles are supported. For more details, please see [the overview section](/content/Basic_Usage/overview.html).

- **Region or GeneID**: The textbox titled "**Region or GeneID** inquire the input for querying genomic regions. The input text shall be in form of `chr:from-to`. For example, `chr1A:1-100`. Also, gene name is acceptable.

- **Flanking region length**: When using the gene name as input, you may want to extend the regions. It is usually `0` bp in the box by default, indicating no flanking region is considered. If `2000` is provided in this input box, then the flanking regions in length of "2000bp" will be included for both upstream and downstream.

- **Draw**: Click for action when getting all options ready.

## Download Options

![Download options](./../img/Download-options-2.gif)

Click the **Download Options** button, and then you can select downloading format (`PNG` or `PDF`) of figure, and specify the width and height to appropriate presentation.

Then, click `Download` to download the figure.

## Details

![PhyloTree channel](./../img/PhyloTree-3.jpg)

There is a table below the plot, showing the distance matrix.

## Demonstration

![Demonstration of PhyloTree](./../img/PhyloTree-0.gif)