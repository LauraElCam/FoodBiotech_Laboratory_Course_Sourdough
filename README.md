# FoodBiotech_Laboratory_Course_Sourdough
This repository contains the data processing scripts, statistical analysis notebooks, and supporting documentation for the **Sourdough Production and Fermentation Analysis practicum (Course 752-5004-00L)** at **ETH Zürich**.

---

# Project Overview

The primary goal of this study is to describe and compare **spontaneous fermentation across different cereal substrates**. By using various flour types as variables, the evolution of the sourdough ecosystem is monitored through three analytical perspectives:

### Physiochemical Analysis
Monitoring **pH** and **Total Titratable Acidity (TTA)**.

### Microbial Count
Tracking the growth and population dynamics of **Lactic Acid Bacteria (LAB)** and **yeasts**.

### Untargeted Metabolite Mapping
Using **LC–MS** to identify how microbial activity shapes the **chemical profile of the dough over time**.

---

# Experimental Design

- **Variables:** Four flour types  
  - Wheat  
  - Spelt  
  - Buckwheat  
  - Maize  

- **Time Points:**  
  Multiple measurements across the fermentation duration to capture metabolic shifts.

- **Methodology:**  
  Primary **untargeted metabolomics** combined with traditional **microbiology** and **acidimetry**.

---

# File Descriptions

## 1. Data Preparation Script

**File:** `FBLC_Sourdough_2026_preparation.ipynb`

**Description:**  
This notebook handles the *dry-lab upstream data processing*. It:

- Cleans raw feature tables  
- Manages metadata  
- Ensures mass spectrometry data is correctly formatted with **InChIKeys** for downstream identification

---

## 2. Statistical Analysis Notebook

**File:** `FBLC_Sourdough_2026.ipynb`

**Description:**  
The main analysis pipeline designed for **Google Colab**. It performs:

### Pre-processing
- Data normalization  
- Scaling  
- Transformation

### Multivariate Statistics
- **PCA**  
- **PLS-DA**

Used to visualize clustering based on **flour type** and **fermentation time**.

### Univariate Statistics
- **Volcano plots** to identify significantly changed metabolites.

### Pathway Analysis
- **Over-Representation Analysis (ORA)** to link metabolites to biological pathways and functions.

---

## 3. KEGG Mapping File

**File:** `kegg_inchikey_mapping.csv`

**Description:**  
A reference dataset used during the statistical analysis.

It maps **KEGG IDs** to **InChIKeys**, enabling:

- Accurate metabolite identification  
- Pathway enrichment analysis

---

## 4. Laboratory Manual

**File:** `2026_FEB_Sourdough_Manual.pdf`  
*(also available as `.docx`)*

**Description:**  
The complete practicum guide containing:

- Theoretical background on **sourdough microbiology**
- Step-by-step **wet-lab protocols**
  - pH and TTA measurements
  - Microbial plating
- The **sampling schedule** used to generate the dataset in this repository

---

## 5. Feature Table and metadata

**File:** `2260227_featureTable_SourDough.csv`  
**File:** `260227_metaData_SourDough.csv` 
*(created using FBLC_Sourdough_2026_preparation`)*

**Description:**  
The complete practicum guide containing:

- Theoretical background on **sourdough microbiology**
- Step-by-step **wet-lab protocols**
  - pH and TTA measurements
  - Microbial plating
- The **sampling schedule** used to generate the dataset in this repository



