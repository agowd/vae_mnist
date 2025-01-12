# Variational Autoencoder for MNIST

This project demonstrates a Variational Autoencoder (VAE) implemented to generate MNIST digit images. A VAE is a type of generative model that learns a probabilistic mapping from a latent space to the data space, making it useful for image generation and representation learning.

## Project Overview
- **Dataset:** MNIST handwritten digits, resized to 14x14 and binarized for training.
- **Model Architecture:**
  - **Encoder:** Two fully connected layers (196 → 128 → 16) with tanh activation.
  - **Latent Space:** 8 dimensions for the mean and 8 for the standard deviation.
  - **Decoder:** Two fully connected layers (8 → 128 → 196) with tanh and sigmoid activations.
- **Training Objective:** 
  - Evidence Lower Bound (ELBO) with a KL divergence term and a reconstruction term using the Bernoulli likelihood.
  - Reparameterization trick for gradient flow through the stochastic latent space.

## Results
- **Reconstruction:** Side-by-side plots of original and reconstructed MNIST images.
- **Generation:** Random samples from the latent space decoded into synthetic MNIST images.
- **Training Curves:** Separate plots for KL divergence and reconstruction loss over training iterations.

## Getting Started
Clone this repository and ensure you have the required dependencies installed.

## Requirements
- Python 3.x
- PyTorch
- NumPy
- Matplotlib

```bash
git clone (https://github.com/agowd/vae_mnist.git)
cd vae-mnist
pip install -r requirements.txt
