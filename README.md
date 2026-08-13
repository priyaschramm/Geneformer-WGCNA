# Geneformer-WGCNA
# Leveraging Foundation Model Embeddings for Gene Network Discovery in ALS

## Overview

This project investigates gene network organization in **amyotrophic lateral sclerosis (ALS)** using bulk RNA-seq data from postmortem human frontal cortex. We compare conventional gene co-expression network analysis with **Geneformer**, a foundation model for transcriptomic data, to explore whether gene embeddings can capture biologically meaningful relationships beyond pairwise expression correlations.

The project combines **Weighted Gene Co-expression Network Analysis (WGCNA)** and **Geneformer gene embeddings** to identify gene programs, hub genes, and ALS-associated biological processes.

## Research Question

Can foundation model-derived gene embeddings identify biologically relevant gene networks in ALS that complement or extend networks identified using conventional co-expression analysis?

## Methods

### 1. WGCNA

Weighted Gene Co-expression Network Analysis (WGCNA) was used as a conventional approach for identifying gene networks from bulk RNA-seq data.

Key steps included:

* Preprocessing and filtering bulk RNA-seq expression data
* Constructing weighted gene co-expression networks
* Identifying gene modules based on expression similarity
* Relating modules to ALS status and other sample traits
* Identifying highly connected hub genes
* Exporting networks for visualization in **Cytoscape**
* Performing functional enrichment analysis of selected modules

### 2. Geneformer

Geneformer was used to generate **gene embeddings** representing relationships between genes based on their learned representations from transcriptomic data.

The analysis included:

* Extracting gene embeddings
* Calculating similarities between gene embeddings
* Constructing a gene similarity network
* Clustering genes into gene programs
* Identifying representative/hub genes within programs
* Performing functional and cell-type enrichment analysis
* Comparing Geneformer-derived programs with WGCNA modules

### 3. Network Comparison

Geneformer-derived gene programs were compared with WGCNA modules to identify:

* Shared genes and biological processes
* ALS-associated pathways
* Overlapping immune and neuronal biology
* Additional gene relationships identified by Geneformer
* Differences between embedding-based and correlation-based network approaches

## Dataset

The analysis uses bulk RNA-seq data from **postmortem human frontal cortex** samples, including ALS and control samples.

The frontal cortex is relevant to ALS because, in addition to motor system pathology, ALS can involve cognitive and behavioral changes associated with cortical dysfunction.

## Repository Structure

```text
Geneformer-WGCNA/
│
├── WGCNA/
│   ├── scripts/
│   ├── figures/
│   ├── results/
│   └── README.md
│
├── Geneformer/
│   ├── scripts/
│   ├── embeddings/
│   ├── results/
│   └── ...
│
├── enrichment/
│   └── ...
│
├── figures/
│   └── ...
│
└── README.md
```

## Key Analyses

### WGCNA

WGCNA identifies modules by grouping genes with similar expression patterns across samples. Module–trait relationships and intramodular connectivity were used to identify ALS-associated modules and hub genes.

### Geneformer Gene Programs

Geneformer embeddings were used to capture relationships between genes in a learned representation space. Similarity between embeddings was used to identify groups of genes with related representations and biological functions.

### Functional Enrichment

Gene sets identified from WGCNA modules and Geneformer programs were analyzed using gene ontology and pathway enrichment approaches to determine their associated biological processes.

## Goals

The primary goals of this project are to:

1. Identify ALS-associated gene networks using WGCNA.
2. Identify gene programs using Geneformer embeddings.
3. Compare embedding-based networks with conventional co-expression networks.
4. Identify genes and biological processes shared between the two approaches.
5. Determine whether Geneformer identifies additional ALS-relevant biology not captured by conventional co-expression analysis.
6. Investigate the potential of foundation models for gene network discovery.

## Results

Geneformer and WGCNA identified overlapping ALS-associated biology, including immune-related processes and shared functional pathways. Geneformer also identified additional gene programs associated with processes such as **lncRNA regulation, histone biology, and neuronal signaling**.

Enrichment of relevant brain cell types and biological processes provided additional support for the biological relevance of Geneformer-derived gene programs.

However, several of the most well-established ALS-associated genes were not among the top genes identified within the Geneformer clusters, highlighting differences between embedding-based and conventional network approaches.

## Technologies

* **Python**
* **R**
* **Scanpy**
* **Geneformer**
* **WGCNA**
* **DESeq2**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Cytoscape**
* **Gene Ontology enrichment analysis**

## Project Context

This project was conducted as part of the **New York Genome Center Summer Internship Program 2026**, with a focus on applying computational approaches to investigate long non-coding RNA and gene network biology in ALS.

## Future Directions

Potential future work includes:

* Further characterization of Geneformer-derived gene programs
* Integration of lncRNA-specific analyses
* Comparison with additional ALS datasets
* Network visualization and comparison in Cytoscape
* Investigation of known ALS genes within Geneformer embedding space
* Fine-tuning Geneformer for ALS-specific transcriptomic representations
* Validation of candidate genes and pathways using independent datasets

## Author

**Priya Schramm**
New York Genome Center Summer Internship — 2026

