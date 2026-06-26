# Differential Expression Analysis of RNA-seq Data

Differential expression analysis of the **pasilla** RNA-seq dataset using **DESeq2** in R.

This project compares differential expression models with and without adjustment for sequencing protocol to evaluate the impact of technical batch effects on transcriptomic analyses.

**Authors**

- Mateus Auza Cruz
- Dorian Napolitano

---

## Overview

RNA sequencing experiments are often affected by technical variation that can obscure biological signals.

Using the **pasilla** dataset, this project compares two negative binomial generalized linear models:

- **Unadjusted model:** `~ condition`
- **Adjusted model:** `~ type + condition`

where:

- **condition** corresponds to untreated versus *pasilla* knockdown samples,
- **type** corresponds to the sequencing protocol (single-read or paired-end).

The objective is to evaluate how adjusting for sequencing protocol affects normalization, statistical inference, and the identification of differentially expressed genes.

---

## Repository Structure

```text
.
├── figures/
│   ├── ma-plots.png
│   ├── pca.png
│   └── volcano-plot.png
├── README.md
├── code.qmd
├── pasilla_gene_counts.tsv
└── transcriptomics-report.html
```

---

## Dataset

The analysis is based on the **pasilla** RNA-seq dataset from Bioconductor.

The repository includes the gene count matrix (`pasilla_gene_counts.tsv`). Sample metadata are obtained from the **pasilla** package during execution.

The dataset contains RNA-seq counts from *Drosophila melanogaster* samples under two experimental conditions:

- Untreated
- *pasilla* knockdown (treated)

---

## Methods

The analysis includes:

- Data preprocessing
- Count normalization with **DESeq2**
- Variance Stabilizing Transformation (VST)
- Principal Component Analysis (PCA)
- Differential expression analysis
- MA plot comparison
- Volcano plot visualization
- Comparison of adjusted and unadjusted statistical models

---

## Software

The analysis was performed in **R** using:

- DESeq2
- pasilla
- tidyverse
- ggrepel
- patchwork
- pheatmap
- gt

---

## Running the Analysis

Render the Quarto document:

```bash
quarto render code.qmd
```

or from R:

```r
quarto::quarto_render("code.qmd")
```

---

# Results Preview

## Principal Component Analysis

Principal component analysis reveals that sequencing protocol is an important source of variation among samples.

![PCA](figures/pca.png)

---

## Volcano Plot

Comparison of differentially expressed genes identified by the adjusted model.

![Volcano Plot](figures/volcano-plot.png)

---

## MA Plots

Comparison of MA plots before and after adjustment for sequencing protocol.

![MA Plots](figures/ma-plots.png)

---

## Main Findings

- Sequencing protocol introduces a measurable technical batch effect.
- Accounting for sequencing type improves differential expression analysis.
- The adjusted model identifies biologically meaningful genes while reducing technical bias.
- PCA confirms that sequencing protocol contributes substantially to sample variability.

---

## Report

The complete Quarto report is available in:

- **transcriptomics-report.html**

The complete analysis can be reproduced from:

- **code.qmd**

---

## References

- Love MI, Huber W, Anders S. (2014). *Moderated estimation of fold change and dispersion for RNA-seq data with DESeq2*. Genome Biology.
- Anders S, Huber W. (2010). *Differential expression analysis for sequence count data*. Genome Biology.
- Bioconductor **DESeq2**.
- Bioconductor **pasilla** dataset.

---

## License

This repository is intended for educational and academic purposes.
