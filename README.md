### Overview
  The prediction results from LSTM and Random Forest on the six MME models and Model 85 were integrated and used to train a new Random Forest model, which maps the combined predictions to the corresponding ground truth values of each model.
  
1-Data_preprocessing:
    Since both Random Forest and LSTM models utilize a sliding window approach for prediction, the effective lengths of the training and testing predictions are shorter than the original input periods. Therefore, the period from April 1, 2006 to December 31, 2040 is defined as the new training set, and April 1, 2050 to November 30, 2080 as the new testing set. Corresponding data are extracted from the LSTM_prediction and RF_prediction results.
    As Model 85 is based on monthly-scale data, its prediction outputs are linearly interpolated to match the daily resolution. The new datasets are stored in the DataSet directory in Excel format with the following file names: stacking_data_model_train_<model_id> and stacking_data_model_test_<model_id>.
    Each dataset includes the following features:
    LSTM predictions based on the original model (LSTM_day)
    RF predictions based on the original model (RF_day)
    LSTM predictions based on Model 85 (LSTM_85)
    RF predictions based on Model 85 (RF_85)

2-Stacking:
    Experiment 1: 
    All four variables were simultaneously input into the model, and Random Forest was used for training and prediction. The prediction accuracy was evaluated against the ground truth values corresponding to each model.

    Experiment 2: 
    The variables LSTM_day and RF_day were input into the model, and Random Forest was applied for training and prediction. The prediction accuracy was evaluated based on the ground truth values corresponding to each model.

### Dependencies & Version
- python = 3.8.18
- pandas = 2.0.3
- matplotlib = 3.7.2
- sklearn = 1.3.0

 
1-Data_preprocessing:
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/github/JYHYL/EART60702-Group3/blob/Stacking/1-data_preprocessing.ipynb)

2-Stacking:
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/github/JYHYL/EART60702-Group3/blob/Stacking/2-Stacking.ipynb)
