# ZECMIP Estimation with CEEMDAN

## Overview
This repository contains the code and data for the ZECMIP (Zero Emissions Commitment Model Intercomparison Project) estimation project using CEEMDAN (Complete Ensemble Empirical Mode Decomposition with Adaptive Noise). The goal is to analyze and interpret temperature and carbon cycle dynamics under zero emissions scenarios.

## Methods

### ZECMIP Context
ZECMIP investigates the "zero emissions commitment" (ZEC), which refers to the climate system's response after CO2 emissions are abruptly halted. 

### CEEMDAN Methodology
CEEMDAN (Complete Ensemble Empirical Mode Decomposition with Adaptive Noise) is used to decompose complex climate signals into intrinsic mode functions (IMFs). This approach allows us to isolate components of variability in temperature and carbon cycle data, such as:
- Long-term trends
- Oscillatory components
- Residual noise

### Data Processing
The analysis involves processing temperature and carbon flux data from ZECMIP experiments. Key steps include:
1. Reading model outputs for temperature and carbon flux.
2. Applying CEEMDAN to decompose the signals.
3. Analyzing the resulting IMFs to identify trends and variability.
4. Generating visualizations to summarize findings.

## Code Description

### Key Files
- **`00_make_zecmip_path_file_v3_(all_variable).ipynb`**: Prepares paths for accessing ZECMIP data files across multiple variables.
- **`constants.py`**: Defines constants used throughout the analysis, such as parameter values and file paths.
- **`emics_01.ipynb`**: Exploring the application of CEEMDAN to EMICS. Results from this are not used in final paper
- **`zecmip_anom_methods_and_issues_v1-v3.ipynb`**: Draft notebooks.
- - **`zecmip_anom_methods_and_issues_v4.ipynb`**: Statistical analusis and figures used in final paper

- **`src/`**: Directory containing Python scripts for modular components of the analysis:
  - `classes.py`: Implements classes for structuring data and processing pipelines.
  - `my_stats.py`: Includes statistical utilities for analyzing trends and variability.
  - `open_zecmip.py`: Handles opening and managing ZECMIP data files.
  - `plotting_functions.py`: Provides functions for generating detailed visualizations.
  - `utils.py`: Contains general-purpose utility functions.
  - `xarray_extender.py`: Adds custom functionality to xarray objects.
  - `zec_calculation_functions.py`: Implements specific calculations for ZECMIP-related metrics.

### Workflow
1. **Data Preparation**: Paths to ZECMIP data are organized and loaded using `00_make_zecmip_path_file_v3_(all_variable).ipynb` and `open_zecmip.py`.
2. **Data Analysis**: Anomaly methods are iteratively developed and refined in the `zecmip_anom_methods_and_issues_v1-v4.ipynb` notebooks.


## Repository Structure
```
.
├── data/                  # Paths and metadata for accessing ZECMIP data
│   └── zecmip_experiment_paths_ensemble_sorted_tas.json
├── outputs/               # Results and plots
├── src/                   # Analysis scripts
│   ├── classes.py
│   ├── my_stats.py
│   ├── open_zecmip.py
│   ├── plotting_functions.py
│   ├── utils.py
│   ├── xarray_extender.py
│   └── zec_calculation_functions.py
├── 00_make_zecmip_path_file_v3_(all_variable).ipynb
├── constants.py
├── emics_01.ipynb
├── zecmip_anom_methods_and_issues_v1.ipynb
├── zecmip_anom_methods_and_issues_v2.ipynb
├── zecmip_anom_methods_and_issues_v3.ipynb
├── zecmip_anom_methods_and_issues_v4.ipynb
└── README.md              # Project documentation
```



