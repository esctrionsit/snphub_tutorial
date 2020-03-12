# Configuration

There is a configuration file called `setup.conf` in the `SnpHub` root directory. Content of the file is shown below.

```R
####################################################
# File paths

# Note: please DON'T end path_datafolder and path_vcfolder with "/"

# Folder that contains all files EXCEPT vcf files.
# Also our output folder, so make sure the write permission is given
path_datafolder = "./test2"

# Folder contains vcf files
path_vcfolder = "./test2"

####################################################
# File names
# All theae files should be in path_datafolder

# file name of gff3 file
name_gff3 = "IWGSC_v1.1_HC_20170706.gff3"

# file name of fasta file
name_fasta = "161010_Chinese_Spring_v1.0_pseudomolecules.fasta"


# file name of fasta file
name_metadata = "sample_names.txt"

# file name of groupdata file
name_groupdata = "groupinfo.txt"

# file name of sample location file
name_sam_location = "sample_location.txt"


# file name of system information file
# use NA without "" to ignore this file
name_sysinfo = NA
#name_sysinfo = "./test/sys_info.txt" 


# file name of UI setting information file
# use NA without "" to ignore this file
name_UIsetting = NA
#name_UIsetting = "./test/Aet.json"

####################################################
# tool application paths
# Need NOT to change them if their PATH are default
path_bcftools = "bcftools"
path_samtools = "samtools"
path_seqkit = "seqkit"
path_tabix = "tabix"


```

## Related files
In the first part, the meaning of the variables are:

- **path_datafolder**: the folder path of **all files** except vcfs. New created files would also be puted here.

- **path_vcfolder**: the folder path of vcf(vcf.gz) files of the resequencing data. **ALL** vcf files in the folder would be **merged together**, and annoated with `gff3` file.

- **path_gff3**: the path of gff3 file, or Generic Feature Format file.

- **path_fasta**: the path of reference genome file, which should be in fasta format.

- **path_metadata**: the path of metadata file. More datail is writen in the next section.

- **path_groupdata**: the path of group information file. More datail is writen in the next section.

- **path_sam_location**: the path of sample location information file. More datail is writen in the next section.

- **path_sysinfo**: the path of system information file. It's value could be NA. More datail is writen in the next section.

- **path_UIsetting**: the path of UI setting file. It's value could be `NA`. More datail is writen in the next section.

## Tool path
In the second part, variables contains the path of 3 tools: `bcftools`, `samtools`, `seqkit` and `tabix`. If the path is default, just leave them then.

But, if the default tool is not fit for `SnpHub`, due to the version problem or somehow, you can change the path to somewhere new.
