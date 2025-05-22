# Autoencoder for Image Denoising with Latent Space Extraction

This project implements convolutional autoencoders to denoise grayscale pneumonia images corrupted with Poisson noise of varying intensity (λ = 25, 50, 75). The goal is to reconstruct clean images from noisy inputs and analyze the latent space representation.

## Features
- Adds Poisson noise at different intensities (λ values).
- Builds convolutional autoencoder with encoding and decoding layers.
- Trains separate models for each noise level.
- Evaluates reconstruction quality using Peak Signal-to-Noise Ratio (PSNR).
- Extracts and saves latent space representations (encoded features) of noisy training data.

## Details
- Input shape: 64×64 grayscale images.
- Architecture:
    - Encoder: Conv2D + MaxPooling layers compress input into latent space.
    - Decoder: Conv2D + UpSampling layers reconstruct the image.
- Loss: Mean Squared Error between output and clean image.
- Optimizer: Adam.
- Metric: PSNR to quantify reconstruction quality.
- Latent space: Extracted from bottleneck layer output; flattened and saved as CSV.

## Results
- PSNR values increase as the model learns to reconstruct noisy images.
- Latent space vectors can be used for further analysis or downstream tasks like classification.

## Potential Improvements
- Experiment with deeper or residual architectures.
- Try alternative loss functions (e.g., perceptual loss).
- Integrate with downstream tasks like medical diagnosis or anomaly detection.

## Notes
- Due to size constraints, the CSV files containing encoded (latent space) images are not included in this repository.
- You can download the files from this [Google Drive link](https://drive.google.com/drive/folders/1og0gsCifTmV0-rrQi__aZOEcbPJFwZ8a?usp=drive_link).
