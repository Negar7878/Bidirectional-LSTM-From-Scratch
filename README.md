# Bidirectional LSTM for Time Series Prediction

This repository contains an implementation of a Bidirectional Long Short-Term Memory (BiLSTM) network for time series prediction, specifically applied to ECG and temperature data. The model is designed for regression tasks, forecasting continuous values based on past observations.

## Model Architecture

The model architecture is based on a Bidirectional LSTM structure, as illustrated below:

![Model Architecture](images/image.png)

- **Input Layer**: The input sequence, represented as multiple time steps (e.g., `x1`, `x2`, ..., `xn`), is fed into the model.
- **Bidirectional LSTM Layers**: Each time step is processed by an LSTM in both directions:
  - **Left-to-right (l2r)** and **right-to-left (r2l)** hidden states are computed.
- **Fully Connected Layer**: The final hidden states from both directions are concatenated and fed into a fully connected layer to make predictions.
- **Output Layer**: The output from the fully connected layer provides the predicted value for the next time step or sequence point. Mean Squared Error (MSE) is used as the loss function to optimize the model for regression tasks.

## Files in this Repository

- `ECG_5_TimeSteps.ipynb`: Jupyter Notebook for time series analysis on ECG data with 5 time steps using the BiLSTM model for regression.
- `ECG_8_TimeSteps.ipynb`: Jupyter Notebook for time series analysis on ECG data with 8 time steps using the BiLSTM model.
- `Temperature_5_TimeSteps.ipynb`: Jupyter Notebook for temperature prediction with 5 time steps using the BiLSTM model.

## Requirements

To run the notebooks, you need the following Python packages:
- `numpy`
- `pandas`
- `matplotlib` (for visualization)

## Usage

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Negar7878/Bidirectional-LSTM-From-Scratch.git
