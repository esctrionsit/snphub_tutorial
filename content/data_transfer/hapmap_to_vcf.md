# Hapmap to VCF

Considering that there are also a lot of SNP array data, we here provide an interface to transfer `.hapmap` format data into `.vcf`.

Before doing that, please make sure that the following software has been installed:
- `Java` (no earlier than Java6)
- `git`

To get data transfered, just useing the following command.
```sh
python snphub/data_transfer/hapmap2vcf.py -i [input hapmap path] -o [output vcf path]
```