**Author:** Claudia Costa  
**Thesis:** *A computational analysis to decipher different transcriptomic signatures regulating gliomas heterogeneity*

## Project Overview
This repository contains the computational data, enrichment results, and network topologies generated for this thesis. The study decodes the transcriptomic landscape regulating the dichotomy between the invasive (**migraSi** / "Go") and proliferative (**migraNo** / "Grow") phenotypes in Glioblastoma (GBM). 

By integrating Differential Gene Expression (DGE) and Gene Set Enrichment Analysis (GSEA) with systems-level network inference, this workflow extracts highly specialized regulatory modules that capture the tumor's invasive machinery.

---

## Repository Structure

The data is organized into four main directories corresponding to the sequential steps of the computational pipeline:

### 1. `DGE/` (Differential Gene Expression)
Contains the baseline transcriptomic profiling comparing the migraSi and migraNo phenotypes.
* **Normalized Counts:** Raw RNA-Seq counts normalized utilizing the `apeglm` shrinkage estimator to handle dispersion and fold-change variance.
* **Gene Lists:** Complete lists of significantly up-regulated and down-regulated genes.
* **Plots:** Volcano plots and expression visualizations highlighting the phenotypic transcriptomic shift.

### 2. `ORA/` (Over-Representation Analysis)
Contains the preliminary functional enrichment analyses.
* **Background Set:** The background set used to compute the enrichment p-values.
* **Results:** Tabular results of the enriched pathways and gene sets.

### 3. `GSEA/` (Gene Set Enrichment Analysis)
Contains the advanced functional profiling utilizing the MSigDB collections.
* **Complete Results:** Full enrichment tables for the **Hallmarks (H)**, **Curated Pathways (C2)**, and **Gene Ontology (C5)** collections.
* **Leading Edge Subsets:** Isolated lists of the specific differential genes driving the enrichment scores within the core pathways.
* **Plots:** Enrichment score visualizations for the most important pathways and gene sets

### 4. `GRNs/` (Gene Regulatory Networks)
Contains the topological network data used to identify context-specific regulatory modules.
* **Extended Pathways:** New regulatory pathways identified via the GSEA network extension.
* **Filtered Network v2 (Edge Lists):** The condition-specific topological edge lists for both the **migraSi** and **migraNo** architectures.

> **Note on Data Availability:** > The complete, unpruned global Gene Regulatory Networks exceed GitHub's standard file size limits. Therefore, only the structurally **Filtered Network v2** edge lists are hosted in this repository.

---

## Reproducibility
The data provided in these directories directly corresponds to the figures, tables, and biological hypotheses presented in the Results chapters of the thesis.
