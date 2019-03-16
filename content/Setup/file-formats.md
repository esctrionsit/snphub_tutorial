# File Formats

To draw the plots, 3 self-defined files need to be added into configuration file.

## Metadata File

In this file, there are 3 columns divided by `\t`. It is used to gives the user a simpler way to select samples.

### Example

```
Sample1    S1    Sample_No.1
Sample2    S2    Sample_No.2
Sample3    S3    Sample_No.3
Sample4    S4    Sample_No.4
Sample5    S5    Sample_No.5
```

### Column Description

![](./../img/Config-1.jpg)

## Gene Index File

In this file, some basic information of gene is recorded. There are 4 columns in totall, without header, divided by `\t`.

### Example

```
CHROM_1    5    125    GeneId100001
CHROM_1    200    384    GeneId100002
CHROM_2    10    138    GeneId200001
```

### Column Description

![](./../img/Config-2.jpg)

## Group Information File

In this file, information of group is recorded. There are 2 columns in totall, without header, divided by `\t`.

### Example

```
Group1    S1,S2,S3
Group2    S4,S5
Group3    S1,S2,S3,S4,S5
```

### Column Description

![](./../img/Config-3.jpg)
