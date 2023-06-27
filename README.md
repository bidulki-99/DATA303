# DATA303

## HW1: Image Generation with off-the-shelf algorithms
Generate awesome images for DATA303 using off-the-shelf generative models. 
== Examples ==
* DALLE2
* Stable diffusion
* Midjourney
* Dezgo
* Your favortie generative models/services

## HW2: MNIST with Gaussians and VAE
1. Learn a multivariate Gaussian and generate samples
2. Learn VAE and generate samples
- a. train Model A. VAE with Conv2d, ConvTranspose2d, kernel_size=4, stride=2, latent_dims = 2
- b. train Model B. Find a model that yields the “checkerboard artifacts”
- c. train Model C. VAE with Conv2d, ConvTranspose2d, kernel_size=3, stride=2, latent_dims = 10
- d. compare Model A, B, C
- e. Interpolation in Latent Space
  - Interpolate 0 and 9 in latent space. (Model A)
  - (quiz) run cell multiple times: “Interpolation in Latent Space”, explain why different results are obtained
- f. Sample Latent Vector from “Prior” (VAE as Generator) (Model A)
  - Compare the prior and the distribution of training data in the latent space
  - Sample Latent Vector from estimated Gaussian

## HW3: MNIST with GANs
1. Learn a GAN (deconv) with 64x64
- Analysis
  - Learning curve
  - Change hyperparameters; learning rate, batch_size, latent_dims
  - Visualize Generated samples
  - Interpolation
  - Visualize generated images using the same latent vectors across epochs

2. Learn a GAN (deconv) with 28x28
- Change the resolution of images: you may want to change the conv, deconv kernel size and the number of layers
- Analysis
  - Learning curve
  - Change hyperparameters; learning rate, batch_size, latent_dims
  - Visualize Generated samples
  - Interpolation
  - Visualize generated images using the same latent vectors across epochs
    
3. Learn a GAN (MLP)
- Modify the provided code and learn a GAN with MLP
- Compare MLP-based GAN and deconv-based GANs
- Analysis
  - Learning curve
  - Change hyperparameters; learning rate, batch_size, latent_dims
  - Visualize Generated samples
  - Interpolation
  - Visualize generated images using the same latent vectors across epochs
    
4. InfoGAN
- Add mutual information/information loss to a GAN (deconv) with 64x64
- Reproduce Figure 2 (a), (c), (d), in infoGAN with latent codes c1, c2, c3
  - InfoGAN paper: https://arxiv.org/pdf/1606.03657.pdf
    - (a) Digit Type
    - (c) Rotation
    - (d) Width
