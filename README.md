
## Title

An Analysis of DNA Methylation Data in the TCGA-BRCA Study Using the Illumina Infinium HumanMethylation27 BeadArray

## Overview

The objective of our analysis was to determine DNA methylation patterns between tumor tissue and normal tissue in a cohort of 27 patients from the TCGA-BRCA study, which used a paired case-control design that allowed us to compare the two types of tissue in the same individuals.

## Data
- Source: The Cancer Genome Atlas (TCGA)
- Size: 27 patients, ~24,000 CpG sites
- Key variables: Beta values for tumor and non-tumor tissue ($0 \leq \beta \leq 1$)

## Methods
- Used Bioconductor package in R to obtain data
- EDA: Volcano plot, principal component analysis (PCA)
- Primary analysis: elastic net regression

## Results
- PCA showed clear separation between normal and tumor tissue
- Even after adjusting for multiple comparisons via FDR, over 600 sites were either hyper- or hypomethylated in tumor tissue
- No clear associations between hyper- and hypo-methylation in tumor tissue and location in the human genome
- For plots, see the complete PDF

## Limitations / Next Steps
- Only used ~0.1% of CpG sites in the entire human genome 
- Need to test external validity of model and whether it effectively generalizes to larger patient samples
- Future analysis could be done consolidating CpG sites into sets based on location

## How to Reproduce
- Download the Bioconductor package in R
- Use the GDCquery function (in the RMD file) to obtain and preprocess data
- Once data has been preprocessed, run the analysis code in the RMD file
