# SeqMaker

In this tag, you can get the sequence of samples by exchanging the mutation into the reference genome sequence.

![SeqMaker tag](./../img/SeqMaker-1.jpg)

## UI

Options here are pretty simple.

- **Variation type to be replaced**: to choose weather to exchange snp or indel variation only, or to exchange all variations.

- **Replace homozygous/heterozygous?**: choose weather to change homozygous mutation only.

- **Samples**: sample names are wanted here. For example, you could input `sample1,sample2,sample3`. Also, if a sample group has been defined by the administrator, which you could see in the `SampleInfo` panel, and all samples in a particular group are needed, you could use `#pre-defined-group-name-1` to add all of the samples in the group pre-defined-group-name1. **NOTE** that a hash mark is needed because the input shoud be **samples** rather than **groups**.

- **Region**: a region is wanted here. Input format should be `chr:from-to`, like `chr1A:1-100`. You could find the avaliable chromsomes and their length in `SampleInfo` panel. Also, gene name is acceptable.