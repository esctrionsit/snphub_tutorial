# Configuration

There is a configuration file named `setup.conf` under the `SnpHub` home directory. Content of the file is shown as below.

```R
####################################################
# File paths

# Note: please DON'T end path_datafolder and path_vcfolder with "/"

# Type of your data format, could be "vcf" or "hapmap"
data_type = "vcf"
# data_type = "hapmap"

# Path of folder contains vcf files
# All of the vcf files will be loaded in the folder
# Could be ignored if the data format is hapmap 
path_vcfolder = "./test2"

# Path of hapmap data file
# Only accept a single file
# Could be ignored if the data format is vcf
path_hapmap = "./example.hmp.txt"


####################################################
# Path of folder contains other files (below).
# Also our output folder, so make sure the write permission has been given
# DO NOT end with "/"
# WRONG demonstration: "./test2/"
path_datafolder = "./test2"

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
#name_sysinfo = "sys_info.txt" 


# file name of UI setting information file
# use NA without "" to ignore this file
name_UIsetting = NA
#name_UIsetting = "Aet.json"

####################################################
# tool application paths
# Need NOT to change them if their PATH are default
path_bcftools = "bcftools"
path_samtools = "samtools"
path_seqkit = "seqkit"
path_tabix = "tabix"


```

#### Related files
In the first part, the meaning of the variables are:

- **data_type**: Type of the variation data. Could be `"vcf"` or `"hapmap"`

- **path_vcfolder**: The folder path of vcf (zipped by `bgzip` as vcf.gz) files of the resequencing data. **ALL** vcf files in the folder would be **merged together**, and annotated with `gff3` file below. This could be ignored if your data format is hapmap.

- **path_hapmap**: path of your hapmap data file. **Note** that we only accept a single hapmap data file for now. Could be ignored if your data format is vcf.

- **path_datafolder**: The folder path of **all files** except vcfs. New created files would also be put here.

- **name_gff3**: The file name of gff3 file, which has the full name called "the Generic Feature Format Version 3" file.

- **name_fasta**: The file name of reference genome file, which should be in fasta format.

- **name_metadata**: The file name of metadata file (the file is built **by user**). For more format details, please see next section.

- **name_groupdata**: The file name of group information file (the file is built **by user**). For more format details, please see next section.

- **name_sam_location**: The file name of sample location information file (the file is built **by user**). For more format details, please see next section.

- **name_sysinfo**: The file name of system information file (the file is built **by user**). Its value could be `NA`. For more format details, please see next section.

- **name_UIsetting**: The file name of UI setting file (the file is built **by user**). Its value could be `NA`. For more details, please see section "*UI Setting*".

#### Tool path
In the second part, variables contains the path of 4 tools: `bcftools`, `samtools`, `seqkit` and `tabix`. 
