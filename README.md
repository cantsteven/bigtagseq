# Guerin et al., 2025: Alcohol and Astrocytes Publication
## Overview
This repository contains code for the data analysis of "Gene Expression Analysis Suggests Critical Role of Astrocytes in Abstinence from Ethanol Dependence" (Guerin et al., 2025)

The primary R markdown file used in this analysis is: 

### bigtagseq_2.Rmd

This R Markdown file documents the tag-seq bulk RNA-seq analysis workflow in R. It covers steps from loading count and metadata tables, organizing sample annotations, filtering and normalizing gene expression data, performing differential expression analysis using DESeq2 for region- and sex-specific contrasts, annotating genes, outputting lists of differentially expressed genes, and generating visualizations including PCA plots, volcano plots, gene count boxplots, and heatmaps. The workflow also includes variance-based gene filtering and module detection using WGCNA for co-expression network analysis.

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
