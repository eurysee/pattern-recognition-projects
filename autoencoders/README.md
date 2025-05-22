# Autoencoders for Image Denoising and Enhancement

This project explores the use of autoencoders for image denoising using classical filters and deep learning techniques. It is divided into two parts:

1. **Denoising Autoencoders** – evaluates the performance of traditional filters.
2. **Improving Autoencoders** – experiments with enhanced neural architectures like residual connections and inception modules.

---

## Dataset

Images used in this project were grayscale chest X-rays taken from the [Kaggle Pneumonia Dataset](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia). Only a subset of test images from the "PNEUMONIA" folder were used, resized to 64×64.

---

## 1. Classical Denoising Autoencoders

This part evaluates traditional image denoising filters under synthetic Poisson noise with different λ (lambda) levels.

### Results

**Evaluating classical filters for λ=25:**
- Mean Blur PSNR: 10.38 dB
- Median Blur PSNR: 10.21 dB
- Bilateral Filter PSNR: 10.33 dB
- Gaussian Blur PSNR: 10.33 dB

**Evaluating classical filters for λ=50:**
- Mean Blur PSNR: 10.40 dB
- Median Blur PSNR: 10.30 dB
- Bilateral Filter PSNR: 10.40 dB
- Gaussian Blur PSNR: 10.36 dB

**Evaluating classical filters for λ=75:**
- Mean Blur PSNR: 10.41 dB
- Median Blur PSNR: 10.32 dB
- Bilateral Filter PSNR: 10.42 dB
- Gaussian Blur PSNR: 10.38 dB


---

## 2. Improving Autoencoders

This section enhances basic autoencoders with:
- **Residual skip connections**
- **Inception modules**

Each model is trained on noisy input (λ=25) and evaluated on the clean test set using Peak Signal-to-Noise Ratio (PSNR).

### Results
- Residual Skip Connections PSNR: 15.36 dB
- Inception Network PSNR: 24.42 dB

## Potential Improvements
- Explore Denoising Diffusion Models as an advanced alternative.
- Combine classical filters with learned neural networks.
- Implement multi-task learning (e.g. pneumonia classification).