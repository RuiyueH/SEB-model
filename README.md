# SEB-model

## Jupyter Notebooks Overview

This directory contains several Jupyter notebooks for modeling and analyzing the Surface Energy Balance (SEB) using both forward and inverse approaches. Below is a summary of each notebook:

### Forward_SEB_model.ipynb
Implements a forward model of the surface energy balance using a 1D heat equation. The notebook simulates temperature profiles in a soil column over time, given known physical parameters and boundary conditions. It uses PyTorch for numerical computation and convolution, and outputs synthetic temperature data at the surface and at a specified depth. Results are saved to text files for use in inverse modeling.

### Inverse_SEB_model_Synthetic_data_1depth.ipynb
Performs inverse modeling to estimate SEB parameters from synthetic temperature data at a single depth. The notebook uses optimization (with backpropagation) to fit model parameters so that the simulated temperature matches the synthetic target. It is designed to be run in Google Colab and supports running multiple optimization trials in parallel for robust parameter estimation.

### Inverse_SEB_model_Synthetic_data_2depths.ipynb
Similar to the single-depth inverse model, but uses synthetic temperature data from two depths. This allows for improved parameter estimation by leveraging more observational constraints. The notebook supports parallel optimization and is suitable for synthetic data experiments.

### Inverse_SEB_model_WestPhoenix.ipynb
Applies the inverse SEB modeling approach to real-world data from the US-WestPhoenix site. It loads observed meteorological and flux tower data, as well as ERA5-corrected forcing data, to estimate SEB parameters that best fit the observed temperature profiles. This notebook demonstrates the application of the inverse model to actual field measurements.

---
For more details on each notebook's workflow and requirements, please refer to the markdown cells and comments within each notebook.