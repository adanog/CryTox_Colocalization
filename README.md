# CryVipTox Colocalization Study

This repository contains scripts and resources for the **quantitative analysis of colocalization between toxins and cellular components** using high-resolution microscopy data. The study focuses on calculating Manders Overlap Coefficients (MOC) to evaluate interactions between Cry toxins and various organelles, leveraging super-resolution imaging techniques and statistical analysis.

## Overview

The repository includes Jupyter notebooks that automate the following tasks:
1. **File Conversion**: Converting Olympus OIB microscopy files to OME-Zarr format for compatibility with advanced analysis workflows.
2. **Super-Resolution and Colocalization Analysis**: Enhancing image resolution using the Mean Shift Super Resolution (MSSR) algorithm and calculating colocalization metrics (M1 and M2) using Manders Overlap Coefficients.
3. **Toxin-Organelle Interaction Analysis**: Comparing colocalization metrics across experimental conditions using statistical methods and visualizations (boxplots and violin plots).

## Key Features

- **OME-Zarr Conversion**: Automated conversion of OIB files to OME-Zarr format with ROI metadata preservation.
- **MSSR Integration**: Application of MSSR for sub-diffraction resolution enhancement.
- **Colocalization Quantification**: Calculation of Manders Overlap Coefficients (M1 and M2) with mathematical rigor.
- **Statistical Analysis**: Use of Kruskal-Wallis H-tests and Tukey's HSD for comparing experimental conditions.
- **Visualization**: Generation of PDF files with boxplots and violin plots for clear data representation.

## Repository Structure

```plaintext
CryVipTox_Colocalization_Study/
│
├── 01_oib2ome-zarr_full_batch.ipynb         # Conversion of OIB files to OME-Zarr format
├── 02_MSSR_Manders_Colocalization_batch.ipynb  # MSSR application and MOC calculations
├── 03_Vesicles_Organels_Toxin-Interaction_Analysis.ipynb  # Statistical analysis and visualizations
│
├── data/                                    # Folder for input microscopy data
├── results/                                 # Output files including PDF plots and statistical summaries
├── README.md                                # Documentation for repository
└── LICENSE                                  # BSD-3-Clause license file
