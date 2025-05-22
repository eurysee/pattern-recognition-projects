# Image Denoising and Smoothing with OpenCV

This project explores classical image denoising techniques using OpenCV.  
The goal is to reduce image noise and smooth visual data while preserving important features like edges.

## Methods Implemented
- **Median Blur**  
  Replaces each pixel with the median of its neighbors. Effective against salt-and-pepper noise.
  
- **Mean Blur (Averaging)**  
  Replaces each pixel with the average of surrounding pixels, producing uniform smoothing.
  
- **Bilateral Filter**  
  Preserves edges by considering both spatial proximity and pixel intensity differences.
  
- **Gaussian Blur**  
  Applies a Gaussian kernel to emphasize closer pixels, resulting in natural smoothing.

## Evaluation Metric
- **Peak Signal-to-Noise Ratio (PSNR)** is used to evaluate image quality post-denoising.
- Higher PSNR values indicate better preservation of the original image quality.

## Key Findings
- The **Bilateral Filter** produced the highest PSNR among the tested methods.
- Its ability to balance spatial and intensity differences helps reduce noise while preserving edges.

## Code Highlights
- Loops through dynamic kernel sizes for comparative analysis.
- Displays each filtered image in real time using OpenCV windows.
- Implements a PSNR calculation function to assess filtering performance.

## Potential Improvements
- Support for batch image processing.
- Option to save filtered outputs for comparison.
- Add more advanced denoising methods (e.g., Non-local Means, wavelet denoising).