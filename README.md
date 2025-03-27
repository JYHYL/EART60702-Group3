# EART60702-Group3
## Stacking Model: Integration of LSTM and Random Forest Predictions
### Overview
    This notebook applies a stacking approach by integrating prediction results from both LSTM and Random Forest models across the six MME ensemble models (003–008) and the CHESS model (085). The combined predictions are used as input features to train a new Random Forest model, mapping them to the corresponding ground truth values.

### Data Preprocessing
    Due to the use of a sliding window strategy in both LSTM and Random Forest models, the resulting prediction sequences are shorter than the full input period. A consistent temporal window is defined for all models:

Training period: April 1, 2006 to December 31, 2040

Testing period: April 1, 2050 to November 30, 2080

#### Key processing steps:

Predictions from LSTM_prediction/ and RF_prediction/ directories are extracted for each model.

As Model 85 (CHESS) operates on a monthly scale, its predictions are linearly interpolated to match the daily resolution of MME models.

#### Final datasets are saved as Excel files in the DataSet/ directory:

stacking_data_model_train_<model_id>.xlsx

stacking_data_model_test_<model_id>.xlsx

#### Each dataset includes the following features:

LSTM_day: LSTM predictions based on the model itself

RF_day: RF predictions based on the model itself

LSTM_85: LSTM predictions from Model 85

RF_85: RF predictions from Model 85

### Stacking Experiments
#### Experiment 1:
All four features (LSTM_day, RF_day, LSTM_85, RF_85) are used as input. A Random Forest model is trained and evaluated against each model's true values.

#### Experiment 2:
Only the model's own LSTM and RF predictions (LSTM_day, RF_day) are used. A Random Forest model is trained and evaluated accordingly.

### Reproducibility
The dataset is loaded directly from GitHub for consistency

To ensure compatibility and reproducibility, the following environment is used:

python: 3.8.18
pandas: 2.0.3
matplotlib: 3.7.2
scikit-learn: 1.3.0

## Notebooks
1-Data_preprocessing:
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/github/JYHYL/EART60702-Group3/blob/Stacking/1-data_preprocessing.ipynb)

2-Stacking:
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/github/JYHYL/EART60702-Group3/blob/Stacking/2-Stacking.ipynb)
