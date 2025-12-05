# RNA-Seq Differential Expression Pipeline – Project Summary

## 1. Objective
The goal of this project is to demonstrate a complete **dry-lab RNA-Seq analysis workflow** using a public dataset from GEO (NCBI).  
This project shows skills in:
- Data acquisition from GEO  
- Quality control and normalization  
- Differential expression analysis  
- Biological result visualization (PCA, volcano plot, heatmap)

---

## 2. Dataset
- Source: GEO public RNA-Seq dataset (example: **GSE183947**)  
- Type: Gene expression counts for two biological conditions (e.g. control vs treatment).

---

## 3. Workflow Overview

### Notebook 1 – `01_data_download.ipynb`
- Uses **GEOparse** to download the GEO series.
- Saves the raw expression matrix into the `data/` folder.

### Notebook 2 – `02_quality_control_normalization.ipynb`
- Loads the count matrix.
- Performs basic QC (boxplots of log-transformed counts).
- Filters low-expression genes.
- Applies TPM-style normalization.
- Saves normalized matrix into `results/tpm_normalized_matrix.csv`.

### Notebook 3 – `03_differential_expression.ipynb`
- Loads normalized counts and a simple metadata table.
- Separates samples into control vs treatment.
- Computes:
  - log2 fold change  
  - p-values  
  - adjusted p-values (FDR)
- Saves full DEG table to `results/differential_expression_results.csv`.

### Notebook 4 – `04_visualization.ipynb`
- Performs PCA for sample clustering.
- Creates a **volcano plot** to highlight significant genes.
- Plots a **heatmap** of the top differentially expressed genes.

---

## 4. Skills Demonstrated

- **Bioinformatics**
  - RNA-Seq pipeline design
  - GEO data handling
  - Differential expression concepts

- **Programming**
  - Python (pandas, numpy, matplotlib, seaborn, scikit-learn)
  - Reproducible Jupyter notebooks
  - Organized project structure (data, notebooks, scripts, results)

- **Analysis & Communication**
  - QC interpretation
  - DEG table generation
  - Clear visualizations (PCA, volcano, heatmap)
  - Written summary for research communication

---

## 5. Future Improvements

- Integrate **DESeq2** or **edgeR** in R for more advanced statistics.
- Add **functional enrichment analysis** (GO / KEGG pathways).
- Extend to multiple conditions or time-series RNA-Seq experiments.
- Wrap steps into a reproducible pipeline (Snakemake / Nextflow).

---

*Author: Kurakula Rakshitha*  
*MSc Bioinformatics, Teesside University (UK)*  
*Open to internships and job opportunities in the US (dry-lab bioinformatics, genomics, AI in healthcare).*
