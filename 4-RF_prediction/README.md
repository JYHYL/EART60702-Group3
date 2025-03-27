# EART60702-Group3
# Random Forest Modelling (Branch: RF)

## Overview
This section applies Random Forest regression to predict maximum daily average temperature (`TREFMXAV_U`) using a variety of climate forcing variables.

## Models Trained
- **Individual Random Forest models** for each of the MME ensemble members (003–008).
- **Separate model trained on CHESS (0085)** for comparison with ensemble models.

## Training Strategy
- Input features: FSNS, PRECT, PRSN, QBOT, TREFHT, UBOT, VBOT
- Output target: TREFMXAV_U
- Time-based splits:
  - Training: 2006–2040
  - Validation: 2041–2049
  - Testing: 2050–2080
- Number of Trees: 30
- Input Sequence Length:
  - MME: 7-days (sliding window)
  - CHESS: 3 months (3 steps)

## Outputs
- `RF.ipynb` — Main notebook for training and evaluation
- `/RF_MME/` — Folder containing RF results for each MME ensemble containing RMSE plots
- `/RF_CHESS/` — Folder containing RF model performance using CHESS dataset containing RMSE plot
- `README.md` — This file

## Results
- RMSE and prediction plots are generated for each model.
- Used later for comparison and model stacking.

## Reproducing the Environment

To recreate this environment with Conda:

```bash
conda env create -f environment.yml
conda activate climate-modeling-env
