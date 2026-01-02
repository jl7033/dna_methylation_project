# Differential DNA Methylation in TCGA Breast Cancer Data

## Overview
This project analyzes DNA methylation differences between tumor and matched normal tissue
in a cohort of 27 patients from the TCGA-BRCA study. A paired case–control design is used
to enable within-individual comparisons across approximately 24,000 CpG sites.

The analysis focuses on identifying systematic methylation changes associated with tumor
status while accounting for the high-dimensional nature of the data.

## Data
- **Source:** The Cancer Genome Atlas (TCGA-BRCA)
- **Sample size:** 27 patients with matched tumor and normal tissue
- **Features:** ~24,000 CpG sites
- **Measurement:** Beta values representing methylation proportion (0–1)

## Methods
- Data access and preprocessing using Bioconductor tools in R
- Exploratory data analysis using principal component analysis (PCA) and volcano plots
- Penalized regression (elastic net) to identify CpG sites associated with tumor status
- False discovery rate (FDR) correction for multiple hypothesis testing

## Results
- PCA revealed clear separation between tumor and normal tissue samples
- After FDR adjustment, over 600 CpG sites exhibited significant hyper- or hypomethylation
  in tumor tissue
- No strong relationship was observed between differential methylation and genomic location

Selected visualizations are available in the accompanying PDF report.

## Limitations and Future Work
- Analysis is limited to a subset (~0.1%) of CpG sites measured by the array platform
- Model generalizability should be evaluated using larger and independent patient cohorts
- Future work could aggregate CpG sites into biologically meaningful genomic regions

## Reproducibility
All analyses were conducted in R. The R Markdown file contains code to download,
preprocess, and analyze the data using Bioconductor and standard statistical packages.

