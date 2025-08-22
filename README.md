# Guerin et al., 2025: Alcohol and Astrocytes Publication
## Overview
This repository contains code for the data analysis of "Gene Expression Analysis Suggests Critical Role of Astrocytes in Abstinence from Ethanol Dependence" (Guerin et al., 2025)

The primary R markdown file used in this analysis is: 
### bigtagseq_2.Rmd

This Quarto file documents the single-nucleus RNA-seq analysis workflow using the Seurat package in R. It covers the steps from data import (reading .h5 count matrices), sample metadata annotation, quality control, filtering, normalization, batch integration with Harmony, clustering, marker gene identification, initial visualization, cell type annotation, and saves a processed Seurat object. 

## Data folder

The Data folder contains the following: 

### big_count_data.csv

This is the raw count matrix. The first column contains gene_ids, and subsequent columns contain counts for each subject id. 

### exp_design.csv

This file countains the experimental design information. Columns include id (maps to the subject id column names in big_count_data.csv), treatment (control or ethanol treatment), sex (male or female), and region (hippo for hippocampus and entor for entorhinal cortex). 

## Dependencies 
The following R packages were used in each Quarto document: 
- tidyverse
- DESeq2
- apeglm
- WGCNA
- EnhancedVolcano
- org.Rn.eg.db
- ggpubr
- pheatmap
- stats
- emmeans
- AnnotationDbi
