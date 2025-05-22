# Pattern Recognition Projects
This repository contains multiple projects and experiments focused on pattern recognition techniques, including supervised neural networks, autoencoders, and image denoising. The projects use PyTorch and TensorFlow/Keras frameworks for model development.

## Contents
### Classical Denoising
- Classical image denoising techniques to reduce image noise and smooth visual data using OpenCV.  

### Denoising Autoencoder
- An autoencoder model designed to remove noise from images, trained on a noisy version of the pneumonia dataset.

### Improved Autoencoder
- A refined version of the denoising autoencoder with architectural enhancements for better reconstruction quality.

### Latent Space Extraction
- Extraction of latent features from the bottleneck layers of autoencoders, flattened and saved as CSV files for further analysis.

### Supervised Neural Networks
- Implementations of neural networks with residual connections, dense skip connections, and attention mechanisms using PyTorch.

### Neural Regression
- A PyTorch-based multilayer perceptron implementation for time series regression on gold price data.


## Getting Started
### Requirements
- Python 3.7+
- PyTorch
- TensorFlow (for autoencoders)
- OpenCV (for image processing)
- NumPy, Pandas, Matplotlib, scikit-learn

## Datasets
- The pneumonia image dataset and large latent space CSV files are not included due to size limitations.
- The pneumonia images dataset can be downloaded externally on the [Chest X-Ray (Pneumonia) Dataset](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia) on Kaggle.
- Large CSV files with latent space features are hosted on [Google Drive](https://drive.google.com/drive/folders/1og0gsCifTmV0-rrQi__aZOEcbPJFwZ8a?usp=drive_link).


## Usage

### Classical Denoising
- Apply classical image denoising methods (e.g., Gaussian blur, median filtering) using OpenCV to reduce noise and smooth images.
- Useful as a preprocessing step before deep learning or other analyses.

### Autoencoders for Image Denoising
- Load pneumonia images, add Poisson noise, and train autoencoders to reconstruct clean images.
- Extract latent space outputs from bottleneck layers for analysis.

### Supervised Neural Networks
- Models include ResidualModel, DenseNet, and AttentionModel.
- Input: 4-dimensional feature vectors
- Output: 2-dimensional predictions with sigmoid activation
- Skip connections and attention mechanisms enhance learning.

### Latent Space Extraction
- Latent space features are extracted from the bottleneck layer outputs of autoencoders.
- These features are flattened and saved as CSV files for downstream tasks like clustering or visualization.

### Neural Regression
- Multilayer perceptron model for time series regression on gold price data.
- Configurable sequence length, prediction length, and training parameters.

## Notes
- Large datasets and CSVs are hosted externally to keep the repository lightweight.
- All completed projects were developed as part of the requirements for a Pattern Recognition university course.
