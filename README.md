# Food Biotechnology Lab (752-5004-00 P) 2026: Sourdough Fermentation Analysis 

## Table of Contents

* [Overview](#overview)
* [Objectives](#objectives)
* [Repository Structure](#repository-structure)
* [Experimental Design](#experimental-design)

  * [Fermentation Setup](#fermentation-setup)
  * [Sampling Strategy](#sampling-strategy)
  * [Analytical Methods](#analytical-methods)
* [Computational Analysis](#computational-analysis)

  * [Data Preprocessing](#data-preprocessing)
  * [Statistical Methods](#statistical-methods)
* [Google Colab](#google-colab)
* [Documentation](#documentation)
* [Project Metadata](#project-metadata)
* [Authors](#authors)

---

## Overview

This repository contains the data, analysis workflows, and documentation for a controlled sourdough fermentation experiment conducted as part of the 2026 Food Biotechnology Laboratory course (752-5004-00 P) at ETH Zurich.

The project investigates the temporal evolution of microbial communities and metabolite profiles in a traditional sourdough system over an 8-day fermentation period. The analysis integrates physicochemical measurements, microbiological assays, and untargeted metabolomics.

---

## Objectives

The study focuses on three primary dimensions:

* **Microbial Dynamics**
  Quantification of lactic acid bacteria and yeast populations over time.

* **Physicochemical Evolution**
  Monitoring of pH and titratable acidity as indicators of acidification.

* **Metabolomic Shifts**
  Comparative analysis of metabolite profiles across fermentation stages.

---

## Repository Structure

```
.
├── Code/
│   ├── FBLC_Sourdough_2026.ipynb
│   ├── FBLC_Sourdough_2026_preparation.ipynb
│   └── kegg_inchikey_mapping.csv
│
├── Data/
│   ├── 260227_featureTable_Sourdough.csv
│   └── 260227_metaData_Sourdough.csv
│
├── Documentation/
│   ├── 2026_FEB_Sourdough_Manual.pdf
│   └── 2026_FEB_Sourdough_Manual.docx
│
└── README.md
```

---

## Experimental Design

### Fermentation Setup

A sourdough system was prepared using a starter culture, flour, and water (50:30:30, w/w). The mixture was incubated at ambient temperature for 7 days.

### Sampling Strategy

Sampling was conducted at defined intervals:

* **Days 0, 1, 3, 5, 7:** pH and TTA measurements
* **Days 1, 7:** Microbial quantification (flow cytometry, agar plating)
* **Days 0, 1, 7:** Metabolomics sampling

### Analytical Methods

* **Microbiology:** Cell counting via flow cytometry and plate-based enumeration
* **Physicochemical Analysis:** pH measurement and titratable acidity
* **Metabolomics:** Untargeted profiling with downstream statistical analysis

---

## Computational Analysis

### Data Preprocessing

* Feature table construction and alignment with metadata
* Data normalization and filtering
* Metabolite annotation using KEGG–InChIKey mapping

### Statistical Methods

* **Volcano Analysis:** Identification of significantly altered metabolites
* **Principal Component Analysis (PCA):** Unsupervised exploration
* **Partial Least Squares Discriminant Analysis (PLS-DA):** Supervised classification
* **Over-Representation Analysis (ORA):** Pathway enrichment

---

## Google Colab

Execute the analysis in a browser environment:

https://colab.research.google.com/drive/15rx9rS-yCsHH0LVrhyLeajAhJr7RvvXs

During execution of the notebook, you will be prompted to upload the required datasets when needed.

The analysis depends on the following files from the `Data/` directory:

* `260227_featureTable_Sourdough.csv`
* `260227_metaData_Sourdough.csv`

Upload these files at the corresponding steps in the notebook when file input is requested.


---

## Documentation

Detailed experimental protocols are provided in: `2026_FEB_Sourdough_Manual.pdf`.

---

## Project Metadata

* **Institution:** ETH Zurich
* **Course:** 752-5004-00 P — Food Biotechnology Laboratory
* **Year:** 2026

---

## Authors

* Laura Campigotto
* Dr. Maria Paula Rueda Mejia
* Michelle Neugebauer
