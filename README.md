# Food Biotechnology Laboratory Course – Sourdough Fermentation Analysis

This repository contains the data processing scripts, statistical analysis notebooks, raw data files, and supporting documentation for the **Sourdough Production and Fermentation Analysis practicum (Course 752-5004-00L)** at **ETH Zürich**.

---

# Project Overview

The objective of this study is to characterize and compare **spontaneous sourdough fermentation across different cereal substrates**. By using different flour types as experimental variables, the evolution of the sourdough ecosystem is monitored using three complementary analytical approaches.

### Physiochemical Analysis
Measurement of **pH** and **Total Titratable Acidity (TTA)** to evaluate acidification dynamics during fermentation.

### Microbial Quantification
Monitoring the population dynamics of **Lactic Acid Bacteria (LAB)** and **yeasts** during fermentation.

### Untargeted Metabolomics
Application of **liquid chromatography–mass spectrometry (LC–MS)** to investigate how microbial activity alters the **metabolic composition of the dough over time**.

---

# Experimental Design

### Experimental Variables

Four cereal substrates were investigated:

- Wheat
- Spelt
- Buckwheat
- Maize

### Fermentation Timepoints

Samples were collected at multiple stages of fermentation to capture **temporal metabolic changes**.

### Analytical Approach

The study combines:

- **Untargeted LC–MS metabolomics**
- **Classical microbiological plating**
- **Acidimetric measurements (pH and TTA)**

to provide an integrated view of sourdough fermentation.

---

# Repository Structure

## 1. Data Preparation Notebook

**File:**  
`FBLC_Sourdough_2026_preparation.ipynb`

**Purpose**

This notebook performs the upstream **data preparation and integration** required before statistical analysis.

Main tasks include:

- Cleaning raw LC–MS feature tables
- Constructing structured sample metadata
- Integrating metabolite annotations (e.g., InChIKeys)
- Preparing analysis-ready datasets

The notebook exports the processed data used in the statistical analysis pipeline.

---

## 2. Statistical Analysis Notebook

**File:**  
`FBLC_Sourdough_2026.ipynb`

**Purpose**

This notebook implements the **metabolomics analysis workflow**, designed to run in **Google Colab**.


### Univariate Analysis

- **Volcano plots** are used to identify metabolites that exhibit significant changes between experimental conditions.


### Pre-processing

Preparation of the metabolomics dataset:

- removal of non-sample injections (e.g., blanks)
- normalization of peak intensities
- scaling and transformation of feature data

### Multivariate Analysis

Dimensionality reduction and pattern detection:

- **Principal Component Analysis (PCA)**  
  Unsupervised exploration of global metabolic variation.

- **Partial Least Squares Discriminant Analysis (PLS-DA)**  
  Supervised analysis used to identify metabolites contributing to differences between fermentation conditions.

### Pathway Analysis

- **Over-Representation Analysis (ORA)** links significant metabolites to biological pathways using KEGG annotations.

---

## 3. KEGG Mapping File

**File:**  
`kegg_inchikey_mapping.csv`

**Purpose**

Reference dataset used for pathway enrichment analysis.

The file maps:

- **KEGG compound identifiers**
- **InChIKeys**

This mapping enables:

- metabolite annotation
- pathway enrichment analysis during ORA.

---

## 4. Laboratory Manual

**File:**  
`2026_FEB_Sourdough_Manual.pdf`  
*(also available as `.docx`)*

**Purpose**

The laboratory manual provides the full experimental protocol for the practicum, including:

- theoretical background on **sourdough microbiology**
- experimental design and fermentation setup
- pH and TTA measurement protocols
- microbial plating methods
- metabolite extraction protocol for LC–MS  analysis.

---

## 5. Processed Data Files

### Feature Table

**File:**  
`260227_featureTable_SourDough.csv`

This table contains the **untargeted metabolomics feature matrix**, including:

- LC–MS peak intensities
- detected metabolite features
- sample injections (including blanks and QC samples)
- metabolite annotations where available.

Each row represents a **metabolic feature**, and each column represents a **sample injection**.

---

### Metadata Table

**File:**  
`260227_metaData_SourDough.csv`

The metadata table describes each LC–MS injection and links it to the experimental design.

Key variables include:

- **file_name** – raw LC–MS data file
- **sample_type** – sample, blank, QC, or conditioning run
- **condition** – flour type
- **timepoint** – fermentation stage
- **group** – biological replicate
- **condition_timepoint** – combined experimental condition

This file is required to correctly group samples during statistical analysis.

---

# Analysis Workflow

The recommended workflow for reproducing the analysis is:

1. Run  
   `FBLC_Sourdough_2026_preparation.ipynb`

   This notebook prepares the **feature table** and **metadata files**.

2. Upload the processed datasets to **Google Colab**.

3. Run  
   `FBLC_Sourdough_2026.ipynb`

   This notebook performs:
   - volcano plot analysis  
   - preprocessing  
   - PCA and PLS-DA  
   - pathway enrichment analysis

---

# Author

Project developed as part of the **Food Biotechnology Laboratory Course** at **ETH Zürich**.
