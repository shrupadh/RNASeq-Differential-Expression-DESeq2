# RNA-Seq Differential Expression Analysis Using DESeq2

## Project Overview

This project demonstrates a complete RNA-seq differential gene expression analysis workflow using the DESeq2 package in R.

The analysis compares pancreatic islet samples from individuals with **Type 2 Diabetes (T2D)** and healthy controls to identify genes showing differential expression.

The project follows a reproducible bioinformatics workflow including data preparation, quality control, statistical analysis, visualization, and interpretation of results.

---

## Research Question

**Which genes are differentially expressed between pancreatic islet samples from individuals with Type 2 Diabetes and healthy controls?**

---

## Dataset

- **Source:** Gene Expression Omnibus (GEO)
- **Accession:** GSE86468
- **Organism:** *Homo sapiens*
- **Tissue:** Pancreatic islets
- **Samples:** 24
  - 16 Type 2 Diabetes
  - 8 Healthy controls

This project uses RSEM expected counts provided with the public dataset. Since DESeq2 requires integer count data, the expected counts were rounded for educational purposes. In production analyses, raw counts generated from tools such as featureCounts would typically be used.

---

## Workflow

The analysis follows these major steps:

1. Load RNA-seq count data
2. Create sample metadata (colData)
3. Prepare the count matrix
4. Convert expected counts to integers
5. Construct the DESeq2 dataset
6. Run differential expression analysis
7. Extract statistical results
8. Perform quality control
9. Generate visualizations
10. Save analysis results

---

## Project Structure

```
RNASeq-Differential-Expression-DESeq2
│
├── data/
│   └── GSE86468 RNA-seq dataset
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

## Methods

### Differential Expression Analysis

Differential expression analysis was performed using the Bioconductor package **DESeq2**.

The analysis included:

- Size factor normalization
- Dispersion estimation
- Negative Binomial generalized linear model fitting
- Wald statistical test
- Benjamini–Hochberg False Discovery Rate (FDR) correction

---

## Visualizations

### MA Plot

The MA plot displays log2 fold change versus mean normalized expression, allowing visualization of expression changes across genes.

![MA Plot](figures/MA_plot.png)

---

### Principal Component Analysis (PCA)

PCA evaluates overall similarity between samples after variance stabilizing transformation.

![PCA Plot](figures/PCA_plot.png)

---

### Volcano Plot

The volcano plot visualizes both the magnitude of gene expression changes (log2 fold change) and statistical significance (adjusted p-value).

![Volcano Plot](figures/Volcano_plot.png)

---

### Dispersion Plot

The dispersion plot illustrates the relationship between gene expression variability and mean normalized counts.

![Dispersion Plot](figures/Dispersion_plot.png)

---

### Boxplot of Normalized Counts

The boxplots show the distribution of normalized gene expression across all samples after DESeq2 normalization.

![Boxplot](figures/Boxplot_Normalized_Counts.png)

---

## Results

A total of **24,875 genes** with non-zero read counts were analyzed.

No genes met the selected statistical significance threshold after multiple testing correction (adjusted p-value < 0.1).

This result does **not** indicate that diabetic and control samples are biologically identical. Rather, it suggests that under the available sample size and variability, the dataset did not provide sufficient statistical evidence to identify significantly differentially expressed genes.

---

## Software

- R
- RStudio
- DESeq2
- Bioconductor
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
- False Discovery Rate correction
- Principal Component Analysis (PCA)
- Data visualization
- Reproducible bioinformatics workflows
- GitHub project organization

---

