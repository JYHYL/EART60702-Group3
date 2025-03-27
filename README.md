# EART60702-Group3

## Exploratory Data Analysis 
### Overview
This notebook conducts an initial exploratory analysis on the combined MME and CHESS dataset (full_dataset.csv). The aim is to understand the distributions, trends, and completeness of key climate variables across ensemble models and the CHESS baseline.

### Dataset
The dataset includes simulations from six MME ensemble models (003–008) and one CHESS model (0085), covering the period from 2006 to 2080.
Features analyzed:
- Maximum urban daily average temperature (TREFMXAV_U)
- Net surface longwave flux (FLNS)
- Net surface shortwave flux (FSNS)
- Precipitation rate (PRECT)
- Snow precipitation rate (PRSN)
- Water vapour mixing ratio (QBOT)
- Reference height temperature (TREFHT)
- Zonal wind (UBOT)
- Meridional wind (VBOT)

### Analysis Performed
- Summary statistics (.describe())
- Null value inspection
- Variable-by-variable distribution plots grouped by model
- Visual consistency checks to identify model discrepancies (e.g., unit mismatches or scaling issues)

### Outputs
- Side-by-side histograms comparing the distribution of each variable across all models
- Identification of any unusual patterns (e.g., outliers, large discrepancies in units or scale)

### Reproducibility
The dataset is loaded directly from GitHub for consistency:
```
df = pd.read_csv('https://raw.github.com/JYHYL/EART60702-Group3/add-final-dataset/full_dataset.csv')
```

To run this notebook locally, ensure the following packages are installed:
- python: 3.11.11
- numpy: 2.0.2
- matplotlib: 3.10.0
- seaborn: 0.13.2
- pandas: 2.2.2




