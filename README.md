# Guerin et al., 2025: BIGtagseq Publication
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
The following R packages were used in the Rmd document: 
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

## References
tidyverse
Wickham H, Averick M, Bryan J, Chang W, McGowan LD, François R, Grolemund G, Hayes A, Henry L, Hester J, Kuhn M, Pedersen TL, Miller E, Bache SM, Müller K, Ooms J, Robinson D, Seidel DP, Spinu V, Takahashi K, Vaughan D, Wilke C, Woo K, Yutani H (2019). "Welcome to the tidyverse." Journal of Open Source Software, 4(43), 1686. doi:10.21105/joss.01686

DESeq2
Love MI, Huber W, Anders S (2014). "Moderated estimation of fold change and dispersion for RNA-seq data with DESeq2." Genome Biology, 15(12), 550. doi:10.1186/s13059-014-0550-8

apeglm
Zhu A, Ibrahim JG, Love MI (2019). "Heavy-tailed prior distributions for sequence count data: removing the noise and preserving large differences." Bioinformatics, 35(12), 2084–2092. doi:10.1093/bioinformatics/bty895

WGCNA
Langfelder P, Horvath S (2008). "WGCNA: an R package for weighted correlation network analysis." BMC Bioinformatics, 9, 559. doi:10.1186/1471-2105-9-559

EnhancedVolcano
Blighe K, Rana S, Lewis M (2019). "EnhancedVolcano: Publication-ready volcano plots with enhanced colouring and labeling." R package version 1.17.0. https://github.com/kevinblighe/EnhancedVolcano

org.Rn.eg.db
Carlson M (2023). org.Rn.eg.db: Genome wide annotation for Rat. R package version 3.18.0. https://bioconductor.org/packages/org.Rn.eg.db/

ggpubr
Kassambara A (2023). ggpubr: 'ggplot2' Based Publication Ready Plots. R package version 0.6.0. https://CRAN.R-project.org/package=ggpubr

pheatmap
Kolde R (2019). pheatmap: Pretty Heatmaps. R package version 1.0.12. https://CRAN.R-project.org/package=pheatmap

stats
R Core Team (2024). R: A language and environment for statistical computing. R Foundation for Statistical Computing, Vienna, Austria. https://www.R-project.org/

emmeans
Lenth RV (2023). emmeans: Estimated Marginal Means, aka Least-Squares Means. R package version 1.8.6. https://CRAN.R-project.org/package=emmeans

AnnotationDbi
Carlson M (2023). AnnotationDbi: Manipulation of SQLite-based annotations in Bioconductor. R package version 1.64.1. https://bioconductor.org/packages/AnnotationDbi/
