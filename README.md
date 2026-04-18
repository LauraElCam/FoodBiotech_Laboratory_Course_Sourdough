# Food Biotechnology Lab: Sourdough Fermentation Analysis

This repository contains the raw data, analysis scripts, and final documentation for the sourdough fermentation experiment conducted as part of the 2026 Food Biotechnology Laboratory course (752-5004-00 P) at ETH Zurich.

---

## Table of Contents
* Project Overview
* Repository Structure
* Methodology
* Prerequisites and Setup
---

## Project Overview
The objective of this laboratory project is to monitor and analyze the biochemical and microbial dynamics of a traditional sourdough starter over a set fermentation period. Key parameters analyzed in this study include:

* **Microbial Population Dynamics:** Tracking the growth of Lactic Acid Bacteria (LAB) and yeast over time.
* **Physicochemical Changes:** Monitoring pH levels and Titratable Acidity to assess acidification.
* **Metabolite Production:** Analyzing the bulk metabolome of sourdough at the start and end of the fermetation.

---

## Repository Structure

The workspace is organized as follows to separate datasets, analysis code, and lab documentation:

* **`Code/`** - Contains all Jupyter notebooks and mapping scripts for the analysis.
  * `FBLC_Sourdough_2026.ipynb` - Main data analysis and visualization notebook.
  * `FBLC_Sourdough_2026_preparation.ipynb` - Data preparation and preprocessing notebook.
  * `kegg_inchikey_mapping.csv` - Mapping file for KEGG and InChIKey identifiers.
* **`Data/`** - Contains the datasets used for the experiment.
  * `260227_featureTable_SourDough.csv` - Primary feature table dataset.
  * `260227_metaData_SourDough.csv` - Metadata corresponding to the sourdough samples.
* **`Documentation/`** - Contains lab manuals and supporting documents.
  * `2026_FEB_Sourdough_Manual.pdf` - Final PDF version of the lab manual.
  * `2026_FEB_Sourdough_Manual 19.36.08.docx` - Word document version of the lab manual.
* **`README.md`** - Main repository documentation.

---

## Methodology

This project encompasses the physical fermentation of the sourdough, microbial and physicochemical monitoring, and the subsequent computational metabolomics analysis. Full wet-lab protocol details can be found in `Documentation/2026_FEB_Sourdough_Manual.pdf`.

### 1. Fermentation Preparation
The sourdough was prepared using a mixture of starter culture, flour, and water in a 50:30:30 ratio by weight. The mixture was then incubated at room temperature for the duration of the 8-day experiment.

### 2. Sampling & Wet-Lab Analysis
Sampling was conducted over the 8-day fermentation period, with specific assays performed at distinct intervals to capture the sourdough's biological and chemical progression:
* **Physicochemical Analysis:** pH and Titratable Acidity (TTA) were measured on **Days 0, 1, 3, 5, and 8** to track the acidification process.
* **Microbial Dynamics:** Cell counting via flow cytometry and traditional agar plating were performed on **Days 1 and 8** to monitor microbial population shifts.
* **Metabolomics Profiling:** Samples for metabolite extraction and downstream instrumental analysis were collected at baseline (**Day 0 / Starter**), as well as on **Days 1 and 8**.

### 3. Computational Data Analysis (Metabolomics)

* **Data Preprocessing:** Raw instrumental outputs from the Starter (Day 0), Day 1, and Day 8 samples were compiled into a clean feature table (`Data/260227_featureTable_SourDough.csv`) and aligned with the corresponding experimental metadata (`Data/260227_metaData_SourDough.csv`).

* **Statistical Modeling & Visualization:** To evaluate the significance of metabolic shifts between Day 1 and Day 8 of the fermentation, the following methods were applied:
  * **Volcano Plots** (to identify significantly altered metabolites)
  * **Principal Component Analysis (PCA)** (for unsupervised data exploration)
  * **Partial Least Squares Discriminant Analysis (PLS-DA)** (for supervised classification of metabolic profiles)
  * **Pathway Enrichment Analysis (ORA)** (to determine over-represented biological pathways)
---

## Prerequisites and Setup

You can review and reproduce the computational data analysis either directly in your browser using Google Colab or on your local machine.

### Run via Google Colab 
**[View and Execute on Google Colab](https://colab.research.google.com/drive/15rx9rS-yCsHH0LVrhyLeajAhJr7RvvXs#scrollTo=KhitduoxuNqF)**

**Important:** To execute the notebook successfully in Colab, you will need to manually upload the following datasets (found in the `Data/` folder of this repository) into your active Colab session:
* **Feature Table:** `260227_featureTable_SourDough.csv`
* **Metadata:** `260227_metaData_SourDough.csv`
