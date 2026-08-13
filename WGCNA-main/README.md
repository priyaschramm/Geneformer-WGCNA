# Weighted Gene Co-expression Network Analysis (WGCNA) of ALS RNA-seq Data 🧬

## Overview

This project implements a **Weighted Gene Co-expression Network Analysis (WGCNA)** workflow to identify gene networks associated with amyotrophic lateral sclerosis (ALS) using bulk RNA-seq expression data.

WGCNA identifies groups of co-expressed genes (**modules**) and evaluates their relationships with clinical traits to uncover biologically relevant disease-associated networks.

This workflow demonstrates the processing, analysis, and visualization of transcriptomic data to identify candidate genes and pathways involved in disease biology.

---

View the complete interactive R Markdown report here:

[WGCNA ALS Analysis Report](https://priyaschramm.github.io/WGCNA/WGCNA_ALS.html)


## Analysis Workflow

The pipeline includes:

### 1. RNA-seq Data Preparation
- Import TPM expression matrix and clinical metadata
- Align expression data with sample information
- Filter low-expression genes
- Prepare data for WGCNA analysis

### 2. Quality Control
- Sample clustering to identify potential outliers
- Principal component analysis (PCA) to evaluate sample relationships

### 3. Weighted Gene Co-expression Network Construction
- Determine optimal soft-thresholding power
- Construct a signed weighted gene co-expression network
- Identify gene modules based on expression similarity

### 4. Module-Trait Analysis
- Correlate gene modules with ALS status and clinical variables
- Identify modules associated with disease-related traits

### 5. Downstream Analysis
- Export module networks for Cytoscape visualization
- Identify highly connected genes within selected modules
- Annotate long non-coding RNAs (lncRNAs) within disease-associated modules

---

## Results

The analysis identified ALS-associated gene modules, including the **red module**, which was further investigated through network visualization.

The `figures/` folder contains example outputs generated during the analysis, including:

- PCA visualization
- Sample clustering dendrogram
- Module-trait correlation heatmap
- WGCNA module dendrogram
- Cytoscape visualization of the red module network

These visualizations demonstrate the progression from expression data to biological network interpretation.

## Repository Structure

```text
WGCNA/
│
├── WGCNA_ALS.Rmd        # Complete WGCNA analysis workflow
├── README.md            # Project documentation
│
├── figures/             # Example plots generated during analysis
│   ├── QC plots
│   ├── module visualizations
│   └── red module Cytoscape network
│
└── results/             # Exported analysis outputs
    ├── module gene lists
    ├── Cytoscape node files
    └── Cytoscape edge files
```

## Tools & Skills

**Programming and Documentation**
- R
- R Markdown

**Bioinformatics**
- WGCNA
- RNA-seq analysis
- Gene expression analysis
- Clinical metadata integration
- Network biology

**Visualization and Network Analysis**
- ggplot2
- igraph
- Cytoscape

---

## Reproducibility

Requirements:
- R ≥ 4.4.1
- WGCNA
- DESeq2
- tidyverse
- ggplot2
- igraph

To reproduce the analysis:

1. Clone this repository
2. Open `WGCNA_ALS.Rmd`
3. Update file paths to the RNA-seq expression matrix and metadata files
4. Knit the R Markdown file to generate the analysis report

---

## Author

**Priya Schramm**  

July 10, 2026

New York Genome Center Computational Biology Internship 2026
