# AI-driven Image Restoration Using Optimization Techniques

## Introduction
This project builds on the "Split Bregmanized Anisotropic Total Variation Model for Image Deblurring" by Huasong Chen et al., extending the research into the domains of denoising and inpainting. The main objective was to evaluate and replicate the performance of the Split Bregman Iteration technique combined with Anisotropic Total Variation (ATV) for denoising noisy images and explore its applicability for inpainting tasks.

## Problem Statement
Image restoration is a critical challenge in digital image processing, often faced with the dual problem of preserving fine details such as edges while effectively removing noise or restoring missing parts. Classical methods struggle to balance noise reduction and edge preservation, making this an ongoing research area.

This study explores a hybrid approach integrating Split Bregman Iteration—a technique well-suited for solving L1-norm optimization problems—with ATV, which is designed to preserve image edges and reduce artifacts. Additionally, the project expands on the traditional denoising focus by applying these techniques to inpainting tasks, which deal with restoring images with missing portions.

## Objectives
1. **Replication**: To replicate the SB-ATV image denoising approach proposed in the original paper and compare it to Isotropic Total Variation (ITV) using MATLAB.
2. **Extension to Inpainting**: To adapt the SB-ATV and SB-ITV methods for inpainting, addressing images with incomplete sections, and assess their performance across different levels of data loss.

## Methodology

### Denoising Using SB-ATV and SB-ITV
- **SB-ATV**: The project began by implementing the Split Bregman Iteration combined with ATV for denoising. The method was applied to images at three noise levels, comparing the performance to the traditional Isotropic Total Variation (ITV) method. 
- **Evaluation Metrics**: Restoration quality was evaluated using Structural Similarity Index (SSIM) and relative error measurements.

### Inpainting with SB-ATV and SB-ITV
- The study extended the denoising model to inpainting. Inpainting is used to restore images with missing pixels, as opposed to noise-corrupted images. Different masks (25%, 50%, and 75% missing) were applied to simulate the loss of image data.
- **Parameter Tuning**: The parameter \( \mu \) controlling the balance between fidelity and regularization was optimized using trial and error for both denoising and inpainting tasks.

## Results

1. **Denoising Performance**: 
   - SB-ATV outperformed SB-ITV in preserving edge details, particularly at low-to-moderate noise levels.
   - As noise levels increased, the performance of both models declined, though SB-ATV still provided superior edge preservation.
   - The experiments on a dataset of 52 grayscale images confirmed these findings.

2. **Inpainting Results**: 
   - SB-ATV and SB-ITV were successfully applied to inpainting tasks. Both methods restored images effectively, though their performance deteriorated as the portion of missing pixels increased.
   - The ATV method showed a slight advantage over ITV in most scenarios.

## Conclusion
The combination of Split Bregman Iteration and ATV was successfully replicated for denoising tasks and extended to inpainting scenarios. The results demonstrated that ATV's ability to preserve edges makes it more effective than ITV, especially in scenarios involving low-to-moderate noise or incomplete data. Future work could investigate the applicability of these methods in more complex image restoration tasks or explore alternative anisotropic methods.

## Technical Skills
- MATLAB for algorithm implementation and optimization
- Image restoration techniques: Denoising, Inpainting
- Optimization techniques: Split Bregman Iteration
- Mathematical models: Anisotropic and Isotropic Total Variation
