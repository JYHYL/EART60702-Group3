# EART60702-Group3
# Temperature Forecasting in Manchester (2050–2080)

This project applies supervised machine learning techniques to predict future daily maximum urban temperatures (TREFMXAV_U) in Manchester between 2050 and 2080. The work focuses on comparing model performance across a multi-model ensemble (MME) of climate simulations, as well as an external reference dataset (CHESS-SCAPE) commonly used in UK climate studies.

The project combines data preprocessing, exploratory analysis, and time series forecasting using both deep learning and traditional machine learning models.

---

## Project Overview

This repository includes:

- Preprocessing of raw `.nc` climate data from CMIP6-style MME models and CHESS-SCAPE
- Conversion, resampling, and alignment of variables and timeframes
- An EDA of the data 
- Training and evaluation of LSTM and Random Forest models
- A stacked ensemble to combine predictions
- Comparison against CHESS-SCAPE projections as a baseline from academic literature

---
## Research Aim

To evaluate whether a stacked ensemble model, incorporating both LSTM and Random Forest predictions, can improve forecasting of future maximum temperatures in Manchester, and how these results compare to widely used CHESS-SCAPE projections.

---

## Data Sources

- Multi-model ensemble `.nc` files simulating future climate scenarios
- CHESS-SCAPE RCP8.5 bias-corrected projections (monthly resolution)
- All data filtered to a central Manchester coordinate (latitude 53.25, longitude -2.5)

Raw data files are not included due to size. Raw CHESS-SCAPE data can be accessed from the [CEDA Archive](https://catalogue.ceda.ac.uk/uuid/8194b416cbee482b89e0dfbe17c5786c/).
Within the code links to the Raw .nc files can be found.

---

## Models Used

- Long Short-Term Memory (LSTM) networks for time series learning
- Random Forest regression models for feature-based predictions
- Stacked ensemble model trained on both outputs

Training:
- LSTM and RF models trained separately on MME simulations
- CHESS-SCAPE data trained and tested independently for comparison

---
## Lisense 
This project is intended for academic use only. Source climate data is the property of their respective providers and is subject to their usage terms.

---
## Reproducing the environment

To recreate this environment with Conda:

```bash
conda env create -f environment.yml
conda activate climate-modeling-env

