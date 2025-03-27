# EART60702-Group3

## LSTM Model Application
### Overview
This notebook documents the application of an LSTM model to the MME ensemble datasets and the CHESS baseline dataset (Model 85), aiming to generate temperature simulations for subsequent stacking analysis.

#### Separate Application of LSTM to the Six MME Datasets
The LSTM model was applied individually to each of the six MME ensemble datasets (Models 003–008) to perform daily-scale simulations. The results were saved as Excel files in the LSTM_MME_prediction/ directory.

#### Application of LSTM to the CHESS Dataset (Model 85)
The LSTM model was applied to the CHESS baseline dataset (Model 085) for monthly-scale simulations. The output was saved as Excel files in the LSTM_CHESS_prediction/ directory.

### Reproducibility
To ensure compatibility and reproducibility, the following environment is used:
df = pd.read_csv('https://raw.github.com/JYHYL/EART60702-Group3/main/DataSet/full_dataset.csv')


To run this notebook locally, ensure the following packages are installed:

python: 3.8.18
pandas: 2.0.3
numpy: 1.24.3
matplotlib: 3.7.2
scikit-learn: 1.3.0
tensorflow: 2.10.0


[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/github/JYHYL/EART60702-Group3/blob/LSTM_prediction/LSTM.ipynb)
