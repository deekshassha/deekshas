# README
# Acute Myeloid Leukemia Heatmap Analysis

Analysis of RNA sequencing data from Shih et al., 2017 focusing on AML model mice samples.

## Overview

This repository contains an R Markdown analysis pipeline for generating heatmaps from RNA sequencing data of Acute Myeloid Leukemia samples. The analysis uses [refine.bio](https://www.refine.bio/) processed data to examine gene expression patterns across 19 AML model mice samples.

## Dependencies

* R environment with required packages:
  + pheatmap
  + magrittr
  + readr
  + dplyr
  + tibble
  + sessionInfo

## Required Files

Before running the analysis, ensure you have:
1. Downloaded the dataset from [SRP070849](https://www.refine.bio/experiments/SRP070849)
2. Created the following directory structure:
```markdown
project_root/
├── data/
│   └── SRP070849/
│       ├── SRP070849.tsv      # Gene expression matrix
│       └── metadata_SRP070849.tsv  # Sample metadata
└── plots/                    # Output directory for visualizations
```

## Usage Instructions

1. Clone this repository
2. Download the required dataset from refine.bio
3. Place the downloaded files in the specified locations
4. Run the R Markdown document to generate:
   - Processed gene expression data
   - Variance-filtered genes
   - Clustered heatmap visualization
   - Session information report

## Output Files

The analysis generates several key outputs:
- `top_90_var_genes.tsv`: Genes filtered by variance (upper quartile)
- `aml_heatmap.png`: Final annotated heatmap visualization
- Session information report for reproducibility

## Citation Information

This analysis utilizes data from Shih et al., 2017 [PMID: 28193779](https://pubmed.ncbi.nlm.nih.gov/28193779/). The methodology has been adapted from the [refine.bio-examples notebook](https