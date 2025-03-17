# Analysis of m6A-related Genes in DepMap Breast Cancer Cell Lines

This repository contains an Rmarkdown report that explores the role of **m6A-related genes** in **breast cancer cell lines** from the **DepMap** dataset. The analysis leverages multi-omics data, including CRISPR dependency scores, gene expression, copy number variation, and mutation data.

---

## Summary of Findings

### **CRISPR Dependency**
- CRISPR knockout of several m6A-related genes (e.g., **ABCF1**, **RBMX**, **EIF3A**, **HNRNPC**, **VIRMA**) is **highly lethal** in DepMap breast cancer lines.  
- Conversely, knockout of genes such as **YTHDF1**, **YTHDC2**, and **FTO** appears **non-lethal** and may even show a **mild proliferative effect**.  
- Overall, m6A-related genes show **greater lethality** in breast cancer lines than the **global dependency average** across all cell lines.

### **Copy Number Variation**
- **IGF2BP1** has the **highest average copy number** among m6A-related genes, with **substantial variation** across breast cancer lines.  
- Most other m6A-related genes show mean copy number values close to the **diploid reference** (log2 ~ 1).

### **Gene Expression**
- Several m6A-related genes, including **RMB15**, **METTL16**, **YTHDC2**, **METTL14**, **IGF2BP2**, and **IGF2BP3**, show **higher expression** in **ER-negative**/**HER2-negative** breast cancer cell lines.  
- Some genes such as **HNRNPC**, **HNRNPA2B1**, **EIF4G2**, and **G3BP1** are **universally highly expressed** across all breast cancer cell lines.

### **Expression vs. Dependency**
- **ABCF1**, **ALKBH5**, and **CBLL1** show a **significant direct correlation** between higher gene expression and stronger dependency, suggesting they are key survival genes in certain breast cancer lines.

### **Mutations**
- **Missense mutations** dominate among m6A-related genes.  
- The gene **VIRMA** (previously known as **KIAA1429**) is the **most frequently mutated** m6A-related gene in DepMap breast cancer lines, though these mutations are **not typically damaging**.  
- **C-to-T** (and **G-to-A**) transitions are **elevated** in metastatic breast cancer cell lines, which may reflect **APOBEC hyperactivity** or **epigenetic dysregulation**.  
- Among metastatic samples, **RBM15** mutations occur **slightly more often** than other m6A-related gene mutations.

---

## Data Sources
- DepMap data was retrieved using the **depmap R package**.
- m6A-related genes were curated from the publication:  
  > Li, Shuang, et al. "Landscape analysis of m6A modification regulators related biological functions and immune characteristics in myasthenia gravis." *Journal of Translational Medicine* 21.1 (2023): 166.

---

## How to Use This Repository
1. Clone this repository:  
   ```bash
   git clone https://github.com/your-username/m6A-breast-cancer-analysis.git
   cd m6A-breast-cancer-analysis
   ```	

## Install dependencies in R
  ```r
  install.packages(c("dplyr", "tidyr", "tibble", "ggplot2", "viridis", "stringr", 
                   "ggrepel", "ggpubr", "depmap", "ExperimentHub", "biomaRt", 
                   "plotly", "pheatmap", "DT"))
  ```
