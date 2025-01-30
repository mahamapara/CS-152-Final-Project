# Assessing performance of VAE and DDPM on Image Synthesis Tasks
Final Project for Tufts Graduate Course on Bayesian Deep Learning (CS-152)

#### This was a joint project, co-authored by Maha Mapara and Tina Wu.

Goal: 
Understand how Denoising Diffusion Probabilistic Models (DDPM) work and explore its advantages and limitations by comparing its performance against Variational Auto Encoders (VAE) on image generation tasks across 2 data sets, MNIST and CIFAR10.

Data: 
MNIST is a simpler, BW clothing image data set.
CIFAR10 is a complex, colored data set of natural images.

Hypothesis:
Given the same training input, DDPM will slightly outperform Convolutional VAE on both data set. By outperform, we mean DDPM will produce better quality images.

Reasoning: Latent variables in DDPM retain the exact dimensionality as the input, while VAE is restricted by a bottleneck layer. Additionally, in VAE information loss is introduced through dimnesionality reductions; regularization of forcing approximated posterior ontp a Gaussian prior distribution can leas to blurry samples for VAE.

Evaluation:
Performance was assessed via sampled image qualities and how well sampled images resemble the input using ELBO to measure model loss and FID scores to quantify image quality.

Conclusion:
VAE outperfomed DDPM on the MNIST data set. We believe this ot be due to its simpler network architectures and notably shorter training time.
DDPM outperfomed VAE on CIFAR10.



