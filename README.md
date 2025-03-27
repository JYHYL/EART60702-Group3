# EART60702-Group3
# Data Preprocessing 

## Overview
This section contains the full pipeline for collecting, cleaning, and merging data from both the CHESS-SCAPE dataset (RCP 8.5) and the MME ensemble (models 003–008). The final output is a merged dataset used across all modelling workflows.

## Data Sources
- **MME Models 003–008**: Daily climate simulations with variables such as TREFHT, PRECT, FSNS, and others.
- **CHESS-SCAPE (RCP85)**: Monthly projections derived from UKCP18, downscaled to 1km resolution.

## Key Preprocessing Steps
- Extracted Manchester grid cell for each dataset.
- Resampled MME daily data to monthly averages for comparability with CHESS.
- Renamed and aligned feature columns across datasets.
- Unit conversions:
  - TREFMXAV_U: Converted from Kelvin to Celsius.
  - PRECT: Standardized where required to match units (checked with source paper).
  - LON: From 0 - 360 to -180 - 180 format for MME
- Added `model` column to track origin (003–008 for MME, 0085 for CHESS).
- Final merged dataset (`full_df`) contains both training and testing periods.

## Output
- `full_df.csv` — Cleaned and merged dataset used for all modelling tasks.
