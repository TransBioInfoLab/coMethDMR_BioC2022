# BioC 2022 coMethDMR Package Workshop

Authors: Gabriel J. Odom, Suky Martinez, Tiago Silva, Ingrid Gonzalez, Fernanda Veitzman, Lissette Gomez, Jermaine Jones, and Lily Wang

Event: coMethDMR Workshop for BioC2022 in Seattle, WA



# Overview
This workshop shows how to use the `coMethDMR::` package for R to detect co-methylated regions of the genome which may be associated with a phenotype of interest. This workshop shows an application related to heroin use. Our paper is here: <https://doi.org/10.1093/nar/gkz590>. Our pacakge website shows other examples: <https://transbioinfolab.github.io/coMethDMR/>.



# Necessary Software and Data Sets
You will need the following packages and data to run the examples in this workshop:

1) The [`coMethDMR`](https://bioconductor.org/packages/release/bioc/html/coMethDMR.html) package
2) A list of genomic regions with close-by CpGs, for Illumina 450k or EPIC arrays
    - the [coMethDMR_data](https://github.com/TransBioInfoLab/coMethDMR_data) repository includes pre-calculated lists of these regions for certain parameter values
    - for this workshop, you will need the file `"EPIC_10b4_Gene_3_200.rds"` in the `data/` directory. The original source for this file is here: <https://github.com/TransBioInfoLab/coMethDMR_data/blob/main/data/EPIC_10b4_Gene_3_200.rds>
3) Sample-matched phenotype and genome data (example semi-synthetic data in `data/`)
4) A cup of coffee (or tea) and a little bit of patience 



# Setup

- Fork and download this repository
- Install `coMethDMR` from [Bioconductor](https://www.bioconductor.org/) with the following commands:

```
if (!require("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("coMethDMR")
```

- Install human genome data packages:

```
BiocManager::install("IlluminaHumanMethylationEPICanno.ilm10b4.hg19")
BiocManager::install("sesameData")
```

- For various supplemental components of the workshop, install the following packages:

```
# General workflow
install.packages("tidyverse")

# Pretty tables of results
install.packages("kableExtra")

# Graphics and Wrangling Genomic Data
install.packages("corrplot")
BiocManager::install("pathwayPCA")
```

