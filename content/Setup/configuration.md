# Configuration

There is a configuration file called `config.R` in the root directory. Content of the file is shown below.

```R
# filepaths
path_fasta <- "./test/Aet_v4.0.fasta"
path_fa_index <- "./test/Aet_v4.0.fasta.fai"
path_gff3 <- "./test/Aet_v4.0.gff3.gz"
path_metadata <- "./test/sample_name.txt"
path_geneindex <- "./test/geneinfo.txt"
path_vcf <- "./test/Aet.ann.bcf.gz"
path_groupdata <- "./test/group_info.txt"
path_sam_location <- "./test/location_info.txt"

#path_sysinfo <- NA
path_sysinfo <- "./test/sys_info.txt"

#path_UIsetting <- NA
path_UIsetting <- "./test/Aet.json"
#tool application paths
path_bcftools <- "bcftools"
path_samtools <- "samtools"
path_seqkit <- "seqkit"
path_tabix <- "tabix"

```

## Related files
In the first part, the meaning of the variables are:
- **path_fasta**: the path of reference genome file, which should be in `fasta format`.

- **path_fa_index**: the path of `fasta index file` of the fasta aforementioned. [Here](https://gatkforums.broadinstitute.org/gatk/discussion/1601/how-can-i-prepare-a-fasta-file-to-use-as-reference) is a tutorial to create one.

- **path_gff3**: the path of gff3 file, or Generic Feature Format file. Make sure it is **indexed**.

- **path_metadata**: the path of metadata file. More datail is writen in the next section.

- **path_geneindex**: the path of gene index file. More datail is writen in the next section.

- **path_vcf**: the path of vcf(vcf.gz) or bcf(bcf.gz) file of the resequencing data. Also, it **should** be **indexed**.

- **path_groupdata**: the path of group information file. More datail is writen in the next section.

- **path_sam_location**: the path of sample location information file. More datail is writen in the next section.

- **path_sysinfo**: the path of system information file. It's value could be NA. More datail is writen in the next section.

- **path_UIsetting**: the path of UI setting file. It's value could be NA. More datail is writen in the next section.

## Tool path
In the second part, variables contains the path of 3 tools: `bcftools`, `samtools`, `seqkit` and `tabix`. If the path is default, just leave them then.

But, if the default tool is not fit for SnpHub, due to the version problem or somehow, you can change the path to somewhere new.
