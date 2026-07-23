# RNA-Seq Differential Expression Analysis Using DESeq2

A reproducible RNA-seq differential gene expression analysis workflow built in **R** using the **DESeq2** Bioconductor package. This project analyzes publicly available pancreatic islet RNA-seq data from individuals with **Type 2 Diabetes (T2D)** and healthy controls.

---

## Project Overview

This project demonstrates a complete RNA-seq differential expression analysis workflow, including:

- Importing RNA-seq count data
- Preparing sample metadata
- Creating a DESeq2 dataset
- Normalizing RNA-seq counts
- Performing differential expression analysis
- Visualizing results
- Exporting analysis results

The goal of this project is to demonstrate a reproducible RNA-seq analysis pipeline using R and Bioconductor.

---

## Research Question

**Which genes are differentially expressed between pancreatic islet samples from individuals with Type 2 Diabetes and healthy controls?**

---

## Dataset

**Source:** Gene Expression Omnibus (GEO)

**Accession:** GSE86468

**Organism:** *Homo sapiens*

**Tissue:** Pancreatic Islets

**Samples**

- 16 Type 2 Diabetes samples
- 8 Healthy control samples

This dataset contains **RSEM expected counts**. For this educational project, the counts were rounded to integers because DESeq2 requires integer count data.

---

## Workflow

```text
RNA-seq Count Data
        │
        ▼
Load Dataset
        │
        ▼
Create Sample Metadata
        │
        ▼
Prepare Count Matrix
        │
        ▼
Create DESeq2 Dataset
        │
        ▼
Normalize Counts
        │
        ▼
Differential Expression Analysis
        │
        ▼
Visualization
        │
        ▼
Export Results
```

---

## Repository Structure

```text
RNASeq-Differential-Expression-DESeq2
│
├── data/
│   └── GSE86468_GEO.bulk.islet.processed.data.RSEM.raw.expected.counts.csv.gz
│
├── figures/
│   ├── MA_plot.png
│   ├── PCA_plot.png
│   ├── Volcano_plot.png
│   ├── Dispersion_plot.png
│   └── Boxplot_Normalized_Counts.png
│
├── notebooks/
│   ├── Differential_Expression_DESeq2.Rmd
│   └── Differential_Expression_DESeq2.html
│
├── results/
│   └── DESeq2_results.csv
│
└── README.md
```

---

# Results

- Analyzed **24,875 genes** with non-zero counts.
- No genes met the selected adjusted p-value threshold after Benjamini–Hochberg false discovery rate correction.
- Successfully normalized RNA-seq count data using DESeq2.
- Generated multiple quality-control and exploratory visualizations.

---

# Visualizations

## MA Plot

Shows the relationship between average normalized gene expression and log2 fold change.

![MA Plot](figures/MA_plot.png)

---

## Principal Component Analysis (PCA)

Visualizes overall variation among RNA-seq samples.

![PCA Plot](figures/PCA_plot.png)

---

## Volcano Plot

Displays both the magnitude of differential expression and statistical significance.

![Volcano Plot](figures/Volcano_plot.png)

---

## Dispersion Plot

Illustrates DESeq2's estimation of gene-wise dispersion.

![Dispersion Plot](figures/Dispersion_plot.png)

---

## Boxplot of Normalized Counts

Shows the distribution of normalized gene expression across all samples.

![Boxplot](figures/Boxplot_Normalized_Counts.png)

---

## Software & Packages

- R
- RStudio
- DESeq2
- Bioconductor
- ggplot2
- R Markdown

---

## Skills Demonstrated

- RNA-seq analysis
- Differential gene expression analysis
- DESeq2
- Bioconductor
- R programming
- R Markdown
- Statistical hypothesis testing
- False Discovery Rate (FDR) correction
- Principal Component Analysis (PCA)
- RNA-seq quality control
- Data visualization
- Reproducible bioinformatics workflows
- Git & GitHub

---

## Future Improvements

- Gene annotation
- Gene Ontology (GO) enrichment analysis
- KEGG pathway analysis
- Automated RNA-seq pipeline using Nextflow
- Interactive visualizations

---
