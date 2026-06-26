# Bioinformatics Data Analysis Portfolio

This repository contains three independent bioinformatics data analysis projects implemented in **R** and documented using **Quarto**. The projects cover core workflows in modern computational biology, including transcriptomics, statistical genomics, and microbiome analysis.

---

## Author

**Mateus Auza Cruz**

### Contributors

- **Dorian Napolitano** (Metagenomics & transcriptomics projects; 50/50 contribution)

---

## Repository Structure

```text
.
├── LICENSE
├── README.md
├── metagenomics/
│   ├── figures/
│   │   ├── dendrogram.png
│   │   ├── pcoa-bray-curtis.png
│   │   ├── pcoa-clusters.png
│   │   └── shannon-diversity.png
│   ├── README.md
│   ├── code.qmd
│   ├── isala_subset.rds
│   └── metagenomics-report.html
│
├── multiple-testing/
│   ├── figures/
│   │   ├── p-value-histogram.png
│   │   └── volcano-plot.png
│   ├── Gollub_SE.rds
│   ├── README.md
│   ├── code.qmd
│   └── multiple-testing-report.html
│
└── transcriptomics/
    ├── figures/
    │   ├── p-value-histogram.png
    │   └── volcano-plot.png
    ├── pasilla_gene_counts.tsv
    ├── README.md
    ├── code.qmd
    └── transcriptomics-report.html
```

---

## Projects Overview

### 1. Transcriptomics Analysis

Differential gene expression analysis using RNA-seq count data from the **Pasilla dataset**.

**Key topics:**
- RNA-seq preprocessing and exploration
- Gene expression filtering
- Differential expression analysis
- Statistical hypothesis testing
- Volcano plots and p-value distributions

**Output:** `transcriptomics-report.html`

---

### 2. Multiple Testing in Genomics

Statistical analysis of leukemia gene expression data comparing **ALL vs AML** samples.

**Key topics:**
- Exploratory data analysis
- Principal Component Analysis (PCA)
- Gene-wise Welch t-tests
- Multiple testing corrections:
  - Bonferroni
  - Šidák
  - Benjamini–Hochberg (FDR)
- Volcano plots and significance analysis

**Output:** `multiple-testing-report.html`

---

### 3. Metagenomics Analysis

Microbiome diversity analysis of vaginal samples from the **ISALA citizen science project**.

**Key topics:**
- Alpha diversity (Shannon, Simpson, richness)
- Beta diversity (Bray–Curtis dissimilarity)
- Principal Coordinates Analysis (PCoA)
- Hierarchical clustering
- Community structure interpretation

**Output:** `metagenomics-report.html`

---

## Technologies Used

- R (tidyverse ecosystem)
- Bioconductor (`SummarizedExperiment`)
- vegan
- ggplot2
- cluster
- factoextra
- patchwork
- gt
- kableExtra
- Quarto

---

## How to Run the Analyses

Each project is self-contained.

Run the following command inside any project folder:

```bash
quarto render code.qmd
```

Or open `code.qmd` in **RStudio** and click **Render**.

---

## Purpose of This Repository

This portfolio demonstrates:

- Statistical analysis of high-dimensional biological data
- Reproducible research practices using Quarto
- Application of bioinformatics methods in:
  - RNA sequencing
  - Microarray analysis
  - Microbiome sequencing

---

## License

This project is licensed under the terms specified in the `LICENSE` file.
