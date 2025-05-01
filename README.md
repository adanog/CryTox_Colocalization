# CryTox Colocalization Study

This repository contains scripts and resources for the **quantitative analysis of colocalization between Cry toxins and intracellular organelles** using high-resolution microscopy. The study computes Manders Overlap Coefficients (MOC) to quantify toxin-organelle interactions, incorporating super-resolution imaging and non-parametric statistical analysis.

## Overview

The repository includes three Jupyter notebooks automating the following tasks:

1. **File Conversion**: Converts Olympus `.oib` microscopy files to OME-Zarr format with ROI metadata.
2. **Super-Resolution + Colocalization**: Applies Mean Shift Super Resolution (MSSR) and calculates Manders' M1 and M2 coefficients.
3. **Statistical Comparison**: Compares MOC values across conditions using non-parametric methods, generating violin plots and PDF summaries.

## Key Features

- **OME-Zarr Support**: Compatible with open bioimaging formats.
- **Super-Resolution Processing**: Integrates MSSR via `napari-superres`.
- **Quantitative Colocalization**: Computes Manders M1 and M2 from ROI-based measurements.
- **Non-parametric Statistics**: Kruskal–Wallis tests with Dunn’s post hoc comparisons (Bonferroni-corrected).
- **Visual Outputs**: Publishes violin plots and p-value tables.

## Sample Data

All microscopy datasets used in this analysis are publicly available at the BioImage Archive:

**Confocal Image Data Repository for the Study**  
*Cite as:* “Cry11Aa Toxin of Bacillus thuringiensis interactions with intracellular organelles in Insect gut Implicating Actin Depolymerization, Massive Endocytosis, and Vesicle Secretion”  
**BioImage Archive Accession**: [S-BIAD1612](https://www.ebi.ac.uk/biostudies/bioimages/studies/S-BIAD1612)

## Installation

Each notebook includes inline `!pip install` commands for required packages. Alternatively, you can install all dependencies using:

```bash
pip install -r requirements.txt
