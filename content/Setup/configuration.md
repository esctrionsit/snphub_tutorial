# Configuration

There is a configuration file called `config.R` in the root directory. Content of the file is shown below.

```R
# filepaths
path_fasta <- "/data2/rawdata2/shinyZavitan/151210_zavitan_v2_pseudomolecules.fa"
path_fa_index <- "/data2/rawdata2/shinyZavitan/151210_zavitan_v2_pseudomolecules.fa.fai"
path_metadata <- "/data2/rawdata2/shinyZavitan/sample_name.txt"
path_geneindex <- "/data2/rawdata2/shinyZavitan/geneinfo.txt"
path_vcf <- "/data2/rawdata2/shinyZavitan/all_emmer_filtered_variants_header_to_SAMN04448013.bcf.gz"
path_groupdata <- "/data2/rawdata2/shinyZavitan/group_info.txt"

#tool application paths
path_bcftools <- "/data/user/shinyug/bin/bcftools"
path_samtools <- "samtools"
path_seqkit <- "/data/user/shinyug/bin/seqkit"

#system
.libPaths(c(.libPaths(), "/home/wangzh/R/x86_64-redhat-linux-gnu-library/3.4"))
```

## Related files
In the first part, the meaning of the variables are:
- **path_fasta**: the path of reference genome file, which should be in `fasta format`.

- **path_fa_index**: the path of `fasta index file` of the fasta aforementioned. [Here](https://gatkforums.broadinstitute.org/gatk/discussion/1601/how-can-i-prepare-a-fasta-file-to-use-as-reference) is a tutorial to create one.

- **path_metadata**: the path of metadata file. More datail is writen in the next section.

- **path_geneindex**: the path of gene index file. More datail is writen in the next section.

- **path_vcf**: the path of vcf(vcf.gz) or bcf(bcf.gz) file of the resequencing data. Also, it **should** be **indexed**.

- **path_groupdata**: the path of group information file. More datail is writen in the next section.

## Tool path
In the second part, variables contains the path of 3 tools: `bcftools`, `samtools` and `seqkit`. If the path is default, then just leave them.

But, if the default tool is not fit for NGBT, due to the version problem or somehow, you can change the path to somewhere new.

## Lib path
The path **need not** to be changed, if all the needed R pachages is installed to the default user. But, if some of the R packages in instelled only by some other user, and you don't want to install it to the default user, add the path to the list.