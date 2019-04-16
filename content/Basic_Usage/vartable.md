# VarTable

There are 2 panels here. The Left one, ①, is the input panel, and the right one is the result display panel.

![VarTable tag](./../img/VarTable-1.jpg)

This function subset the VCF file by the requirements given in the left (①), and shows the result on the right as a table.

**Note** that all the conditions are connected by **logic AND (&&)**

## There are several inputs on the left:

- **Variation Type**: select one of the three ratios that represent `SNP (Single Nucleotide Polymorphism) only`, `indel (input/delete) only` or `snp + indel`.

- **Optional information**: there are 3 check boxes, and additional information would display by selecting them. For more information, check the vcf format document [here](https://samtools.github.io/hts-specs/VCFv4.2.pdf).

- **Samples**: sample names are wanted here. For example, you could input `sample1,sample2,sample3`. Also, if a sample group has been defined by the administrator, which you could see in the `SampleInfo` panel, and all samples in a particular group are needed, you could use `#pre-defined-group-name-1` to add all of the samples in the group pre-defined-group-name1. **NOTE** that a hash mark is needed because the input shoud be **samples** rather than **groups**. **Make sure** that samples only appear **ONCE** in totall.
	- **List of samples, must have variant**: samples here will be asked to have mutations in the result. If they do not have in some postion, these sites won't appear.
	- **List of samples, must NOT have variant**: contrary to the former, postions which samples here have mutations will be deleted. So that samples here won't appear to have mutations in the result.
	- **List of samples, independent of having variant**: samples here won't be dealed, just display.

![Samples of VarTable](./../img/VarTable-2.jpg)

- **Region**: a region is wanted here. Input format should be `chr:from-to`, like `chr1A:1-100`. You could find the avaliable chromsomes and their length in `SampleInfo` panel. Also, gene name is acceptable.

- **Flanking region length**: when you want to use the gene name as region, you may want some extra postions in the upstream or downstream. Value here is simply added to the maximum , and subtracted from the minimum of the region.

- **Advanced Options**: click this button to show/hide some advanced options. **Note** that when these options are hide, they **won't** affect the result.

## RUN, and Download

![Result of VarTable](./../img/VarTable-3.jpg)

Click the `Run` button when get all options ready. Table on the right will show the result of subsetting, or some error message if the input isn't correct.

Click `Download raw results as csv` to download current result shown on the right as csv file.

Click `Download genotype in nucleotide as csv` to download a csv file, contains the genotype in nucleotide.

## Advanced Options

![Advanced options of VarTable](./../img/VarTable-3.jpg)

Click the button `Advanced Options`, and then some more options appeared.**Note** that when these options are hide, they **won't** affect the result.

- **Minimum allele frequency (MAF)**: Minor allele frequency (MAF) is the frequency at which the second most common allele occurs in a given population. Larger the value is, lesser the result postions are. If the value is 0 (by default), this filter function is disabled.

- **Biallelic sites only**: A **biallelic** site is a specific locus in a genome that contains two observed alleles, counting the reference as one, and therefore allowing for one variant allele. A **multiallelic** site is a specific locus in a genome that contains three or more observed alleles, again counting the reference as one, and therefore allowing for two or more variant alleles. Select `Yes`, all postions in the result that have multiallelic will be deleted.

- **Maximum missing rate**: filter option of maximum missing rate.