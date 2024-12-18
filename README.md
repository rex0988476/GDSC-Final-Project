# CE6146 Introduction to Deep Learning Final Project: Predict drug sensitivity with different drugs on cancer cell lines.

## Overview
This repository contains the code, documentation, and visualizations for the CE6146 Final Project. The project uses the Genomics of Drug Sensitivity in Cancer (GDSC) dataset to predict LN_IC50 (the natural log of the half-maximal inhibitory concentration) based on the genetic features of cell lines, aiming to evaluate drug sensitivity.

---

## Table of Contents
1. [Project Objectives](#project-objectives)
2. [Datasets](#datasets)
3. [Usage in Google Colab](#usage-in-google-colab)
5. [Methods and Models](#methods-and-models)
6. [Results](#results)
7. [Reproducibility](#reproducibility)
8. [Contributors](#contributors)
9. [License](#license)

---

## Project Objectives
- Predict drug sensitivity with a focus on estimating the effectiveness of different drugs on cancer cell lines.

---

## Datasets

**Genomics of Drug Sensitivity in Cancer (GDSC)**  
Source: [Dataset Link](https://www.kaggle.com/datasets/samiraalipour/genomics-of-drug-sensitivity-in-cancer-gdsc)

---

## Usage in Google Colab
1. **Open the Notebook**:
   - Click on the Colab badge next to the desired Notebook below to open it in Google Colab:
     - [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rex0988476/GDSC-Final-Project/blob/main/model.ipynb) `model.ipynb`

2. **Run the Notebook**:
   - Execute the cells sequentially to preprocess data, train models, and generate results.

3. **Access Datasets**:
   - The datasets are automatically downloaded from Kaggle during execution. No additional setup is required.

4. **Modify Code**:
   - You can modify and experiment directly within Colab for your custom needs.

---

## Methods and Models
- **Features**:
  - `CNA`: Data on gene copy number changes in the cell line.
  - `Methylation`: Data on DNA methylation patterns in the cell line.
  - `Microsatellite instability Status (MSI)`: Indicates the cell line's MSI status.
  - `Cancer Type (matching TCGA label)`: Cancer type according to TCGA classification.
  - `GDSC Tissue descriptor 1`: Primary tissue type classification.
  - `GDSC Tissue descriptor 2`: Secondary tissue type classification.
  - `PUTATIVE_TARGET`: The presumed molecular target of the drug.
  - `PATHWAY_NAME`: The biological pathway affected by the drug.
  - `TARGET_PATHWAY`: The biological pathway(s) targeted by the drug.
  - `DRUG_NAME`: Name of the drug compound.
  - `MIN_CONC`: Minimum concentration of the drug used in the experiment.
  - `MAX_CONC`: Maximum concentration of the drug used in the experiment.
  - `Screen Medium`: The growth medium used for culturing the cell line.
- **Techniques**: Regression.
- **Models**:
  - XGBoost
  - Random Forest

---

## Results
The following table summarizes the evaluation metrics for the two models used in the project:

| Model | Train Mean Squared Error (MSE) | Test Mean Squared Error (MSE) | Train R-Square | Test R-Square |
|-|-|-|-|-|
| XGBoost | 0.0031 | 0.0031 | 0.7967 | 0.7953 |
| Random Forest | 0.0028 | 0.0030 | 0.8130 | 0.7996 |

Visualizations and analysis outputs are embedded within the Jupyter Notebooks.

---
