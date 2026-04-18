# Food Biotechnology Lab (752-5004-00 P) 2026: Sourdough Fermentation Analysis 

## Table of Contents
* [Overview](#overview)
* [Repository Structure](#repository-structure)
* [Objectives](#objectives)
* [Experimental Design](#experimental-design)
* [Computational Analysis](#computational-analysis)
* [Documentation & Materials](#documentation--materials)
* [Project Information](#project-information)

---

## Overview
This repository contains the data, analysis workflows, and documentation for a controlled sourdough fermentation experiment conducted as part of the 2026 Food Biotechnology Laboratory course (752-5004-00 P) at ETH Zurich.

The project investigates the temporal evolution of microbial communities and metabolite profiles in a traditional sourdough system over an 8-day fermentation period. The analysis integrates physicochemical measurements, microbiological assays, and untargeted metabolomics.

---

## Repository Structure

    .
    ├── Code/
    │   ├── FBLC_Sourdough_2026.ipynb
    │   ├── FBLC_Sourdough_2026_preparation.ipynb
    │   └── kegg_inchikey_mapping.csv
    │
    ├── Data/
    │   ├── 20260225_sequence_list.csv
    │   ├── 260227_featureTable_Sourdough.csv
    │   ├── 260227_metaData_Sourdough.csv
    │   ├── Sirius_structure_identifications.csv
    │   └── mzMine_SourDough_full_feature_table.csv.zip
    │
    ├── Documentation/
    │   ├── 2026_FEB_Sourdough_Manual.pdf
    │   ├── 2026_FEB_Sourdough_Manual.docx
    │   └── practicum.pptx
    │
    └── README.md

---

## Objectives
The study focuses on three primary dimensions:
* **Microbial Dynamics:** Quantification of lactic acid bacteria and yeast populations over time.
* **Physicochemical Evolution:** Monitoring of pH and titratable acidity as indicators of acidification.
* **Metabolomic Shifts:** Comparative analysis of metabolite profiles across fermentation stages.

---

## Experimental Design
A sourdough system was prepared using a starter culture, flour, and water (50:30:30, w/w). The mixture was incubated at ambient temperature for 7 days. Detailed experimental protocols are provided in the manual located in the `Documentation/` folder.

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

### 1. Data Preparation (`FBLC_Sourdough_2026_preparation.ipynb`)
This notebook is used to process raw outputs into usable dataframes:
* **Feature Table Creation:** Utilizes `Sirius_structure_identifications.csv` and `mzMine_SourDough_full_feature_table.csv.zip` to generate the final aligned feature table (`260227_featureTable_Sourdough.csv`).
* **Metadata Creation:** Utilizes `20260225_sequence_list.csv` to generate the finalized metadata file (`260227_metaData_Sourdough.csv`).

### 2. Main Analysis (`FBLC_Sourdough_2026.ipynb`)
This notebook handles data normalization, filtering, and statistical exploration. When prompted, you will need to upload the processed files from the `Data/` directory (`260227_featureTable_Sourdough.csv` and `260227_metaData_Sourdough.csv`).

The computational workflow is divided into two main Jupyter Notebooks, which can be executed in a Google Colab browser environment:
[Google Colab Environment](https://colab.research.google.com/drive/15rx9rS-yCsHH0LVrhyLeajAhJr7RvvXs)

**Statistical Methods included:**
* **Volcano Analysis:** Identification of significantly altered metabolites.
* **Principal Component Analysis (PCA):** Unsupervised exploration.
* **Partial Least Squares Discriminant Analysis (PLS-DA):** Supervised classification.
* **Over-Representation Analysis (ORA):** Pathway enrichment (Note: This specific analysis requires the `kegg_inchikey_mapping.csv` file found in the `Code/` directory).


---

## Documentation & Materials
The `Documentation/` folder contains essential reading and lecture materials:
* **Manuals:** `2026_FEB_Sourdough_Manual` (PDF and Word formats) detailing the lab protocols.
* **Lecture Slides:** `practicum.pptx` contains the PowerPoint presentation for the metabolomics data analysis lecture.

---

## Project Information
* **Institution:** ETH Zurich
* **Course:** 752-5004-00 P — Food Biotechnology Laboratory
* **Year:** 2026
* **Authors:** Laura Campigotto, Dr. Maria Paula Rueda Mejia, Michelle Neugebauer
