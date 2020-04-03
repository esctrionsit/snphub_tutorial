# SeqMaker, create consensus sequence

In this channel, you can create a consensus sequence by substituting variants based on the reference genome, and the result can be downloaded directly as FASTA file.

![SeqMaker channel](./../img/SeqMaker-1.jpg)

## UI

Options here are pretty simple.

- **Variation type to be replaced**: To choose whether to exchange **`snp`** or **`indel`** variation only, or to exchange all variations.

- **Replace homozygous/heterozygous?**: Choose whether to *only replace homozygous mutations*, or *replace both types together*.

- **Samples**: The textbox titled "Samples" inquiry a sample list for querying. Three styles are supported for the sample-list input box, which are 
`list of sample names (Accession name according to the “SampleInfo” channel)`, `use group IDs with "#"` and `mixture`. For more details, please see [the overview section](/content/Basic_Usage/overview.html).
	- **Note:**  **#RAW** is a **RESERVED** ID presents to retrieve the REF (reference genome) sequence directly.

- **Region or GeneID**: The textbox titled "**Region or GeneID** inquires the input for querying genomic regions. The input text shall be in form of `chr:from-to`. For example, `chr1A:1-100`. Also, gene ID is acceptable.

## Demonstration

![Demonstration of SeqMaker](./../img/SeqMaker-0.gif)