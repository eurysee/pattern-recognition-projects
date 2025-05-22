# Neural Regression with PyTorch

This project demonstrates a simple multilayer perceptron (MLP) regression model that predicts future gold prices using time series data. It uses PyTorch to build, train, and evaluate a neural network that learns from sequential price patterns.

---

## Dataset

The model uses [gold price data](https://raw.githubusercontent.com/ralampay/pattern-recognition-course/master/notebooks/FINAL_USO.csv), which includes daily open, high, low, and closing prices.

---

## Problem Statement

Given a sequence of previous prices (e.g., 5 days), predict the next few prices (e.g., next 3 days). This is framed as a regression problem over time series data.

---

## Pipeline Overview

### 1. Data Loading & Visualization

- Loads gold price data into a pandas DataFrame.
- Plots a specific attribute (e.g., `'Low'`, `'Close'`, etc.) to visualize the time series.

### 2. Data Preprocessing

- Uses a sliding window approach to convert the time series into input-output pairs for training.
- Example: Given 5 time steps as input (`X`), predict the next 3 steps (`Y`).
- Splits data into training and testing sets.

### 3. Model Architecture

A simple Multilayer Perceptron (MLP) with:

- Input layer: Equal to the sequence length.
- Hidden layer: 25 neurons (customizable).
- Output layer: Predicts future prices.

Includes versions using different activation functions: ReLU, tanh, sigmoid.

```python
class MultiLayerPerceptron(nn.Module):
    def __init__(self, input_size, hidden_size, output_size):
        ...
```

### 4. Training
Trains the model using:
- Mean Squared Error (MSE) loss.
- Adam optimizer.
- Prints loss at each epoch.

### 5. Prediction & Evaluation
- After training, the model predicts prices for the test set.
- Results are plotted to visually compare predictions vs ground truth.

### Potential Improvements
- Add LSTM/GRU for better sequential modeling.
- Implement cross-validation.
- Normalize data for faster convergence.