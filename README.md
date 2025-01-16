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

plaintext
CryVipTox_Colocalization_Study/
│
├── 01_oib2ome-zarr_full_batch.ipynb         # Conversion of OIB files to OME-Zarr format
├── 02_MSSR_Manders_Colocalization_batch.ipynb  # MSSR application and MOC calculations
├── 03_Vesicles_Organels_Toxin-Interaction_Analysis.ipynb  # Statistical analysis and visualizations
│
├── ...                                 
├── ...                              
├── README.md                                # Documentation for repository
└── LICENSE                                  # BSD-3-Clause license file

## Installation

To run the notebooks, ensure the following dependencies are installed:

- Python 3.8+
- Jupyter Notebook
- Required Python libraries:
  ```plaintext
  numpy
  pandas
  matplotlib
  scipy
  statsmodels
  skimage
  natsort
  ome-zarr
  oiffile
  read_roi
  roifile
  napari-superres
  zarr

You can install the dependencies using pip:
pip install numpy pandas matplotlib scipy statsmodels scikit-image natsort ome-zarr oiffile read_roi roifile napari-superres zarr



## Usage

### Prepare Input Files
- Place Olympus OIB files and associated ROI zip files in the `data/` directory (you need to create the directory).

### Run the Notebooks
- Open and execute the Jupyter notebooks in the provided order:
  1. `01_oib2ome-zarr_full_batch.ipynb`: Converts OIB files to OME-Zarr format.
  2. `02_MSSR_Manders_Colocalization_batch.ipynb`: Applies MSSR and calculates MOC.
  3. `03_Vesicles_Organels_Toxin-Interaction_Analysis.ipynb`: Analyzes and visualizes toxin-organelle interactions.

### View Results
- Processed OME-Zarr files, statistical outputs, and visualization PDFs will be saved in the `results/` directory.

## Citation

If you use this repository for your research, please cite:

- López-Molina et al., 2025. "In Vivo High-Resolution MSSR Microscopy Uncovers the Intoxication pathway of Bacillus thuringiensis Cry Toxins in insect gut implicating Actin Depolymerization, Massive Endocytosis, and Vesicle Secretion" *Manuscript in preparation*.

## License

This repository is licensed under the **BSD-3-Clause license**. See the [LICENSE](./LICENSE) file for details.

## Contact

For questions or feedback, please contact the repository maintainers via [GitHub Issues](https://github.com/adanog/CryVipTox_Colocalization_Study/issues).
```
