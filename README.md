# Gene-co-expression-network-analysis
This repository includes workflows for analyzing the gene co-expression networks.

## 1. Analytical Architecture:
# Network Construction: 
Implementation of a weighted adjacency matrix to emphasize high correlations and dampen low correlations, preserving the continuous nature of gene expression.
# Topology Analysis: 
Selection of the Soft-Thresholding Power (β) using the Scale-Free Topology Criterion (R^2 > 0.80 or 0.90).
# Module Identification: 
Utilizing Dynamic Tree Cut algorithms on Hierarchical Clustering dendrograms to identify co-expression modules.
# Biological Significance: 
Calculating Module Eigengenes (ME).


## 2. Method
Weighted Gene Co-expression Network Analysis (WGCNA)

Reference:
Langfelder, P., & Horvath, S. (2008). WGCNA: an R package for weighted correlation network analysis. 

## 3. Analysis Workflow
1. Import gene expression data
2. Construct co-expression modules
3. Visualization

## 4. Tools
- R
- WGCNA package

## 5. Related Repositories
- Downstream-functional-analysis (GO, promoter, miRNA)

```mermaid
graph TD
    A[Cleaned Expression Data] --> B[Pick Soft-Thresholding Power]
    B --> C[Calculate Adjacency & TOM]
    C --> D[Hierarchical Clustering]
    D --> E[Identify Co-expression Modules]
    E --> F[Relate Modules to the Traits]


