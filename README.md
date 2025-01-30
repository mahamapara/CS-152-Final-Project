# Assessing performance of VAE and DDPM on Image Synthesis Tasks
Final Project for Tufts Graduate Course on Bayesian Deep Learning (CS-152)

#### This was a joint project, co-authored by Maha Mapara and Tina Wu.

### Motivation:
- Diffusion models are currently an exciting area of research in generative models, especially for image synthesis tasks; many popular architectures use diffusion models for this purpose, like DALLE-2 and Imagen. This was a good opportunity to gain in-depth exposure about the architecture and modeling approach used for diffusion models. In particular, we were inspired by the paper ‘Diffusion Models Beat GAN on Image Synthesis’ [Dhariwal and Nichol (2021)], where the authors compare DDPM performance with GANs on image synthesis using ImageNet and LSUN image data. Instead of comparing DDPM to GAN, we compared diffusion models with VAEs. This is because:
  1. We have not seen a comparison between VAE and diffusion models in the literature on our choice of data sets.
  2. The models have some similarities:
    • Forward process that turns data into latent representations
    • Reverse process that involves sampling some latent variable
    • Training objective which is a lower bound on data likelihood
  3. It would be interesting to see how different the model performances are, and evaluate the expected underperformance of VAEs based on our understanding of the key differences between DDPMs and VAEs.


### Goal: 
- Understand how Denoising Diffusion Probabilistic Models (DDPM) work and explore its advantages and limitations by comparing its performance against Variational Auto Encoders (VAE) on image generation tasks across 2 data sets, MNIST and CIFAR10.

### Data: 
- MNIST is a simpler, BW clothing image data set.
- CIFAR10 is a complex, colored data set of natural images.

### Hypothesis:
- Given the same training input, DDPM will slightly outperform Convolutional VAE on both data set. By outperform, we mean DDPM will produce better quality images.

### Reasoning: 
- Latent variables in DDPM retain the exact dimensionality as the input, while VAE is restricted by a bottleneck layer. Additionally, in VAE information loss is introduced through dimnesionality reductions; regularization of forcing approximated posterior ontp a Gaussian prior distribution can leas to blurry samples for VAE.

### Evaluation:
- Performance was assessed via sampled image qualities and how well sampled images resemble the input using ELBO to measure model loss and FID scores to quantify image quality.

### Conclusion:
- VAE outperfomed DDPM on the MNIST data set. We believe this ot be due to its simpler network architectures and notably shorter training time.
- DDPM outperfomed VAE on CIFAR10.



