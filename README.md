# DCGAN on CelebA Faces

This project implements a **Deep Convolutional Generative Adversarial Network (DCGAN)** trained on the **CelebA dataset** to generate realistic human face images. The implementation is done in **TensorFlow/Keras** and follows the architecture introduced in the [DCGAN paper (Radford et al., 2015)](https://arxiv.org/abs/1511.06434).



## 📌 Overview
- Trains a Generator and Discriminator in an adversarial setup
- Generator learns to map random noise vectors to realistic face images
- Discriminator distinguishes between real CelebA faces and generated ones
- Saves generated image grids during training and plots loss curves


## 📂 Dataset
- **Source**: [CelebA Dataset on Kaggle](https://www.kaggle.com/datasets/jessicali9530/celeba-dataset)  
- **Type**: Human face images (over 200,000 samples)  
- **Image size**: 64×64, RGB  
- **Preprocessing**:
  - Resized to 64×64
  - Normalized to [-1, 1]
  - Shuffled and batched



## ⚙️ Model Architecture

### Generator
- Input: latent vector of size **100**
- Dense → reshape to **4×4×100**
- Conv2DTranspose layers with [512, 256, 128] filters
- BatchNormalization + LeakyReLU activations
- Output: 64×64×3 image with **Tanh** activation

### Discriminator
- Input: **64×64×3** image
- Conv2D layers with [64, 128, 256] filters
- BatchNormalization + LeakyReLU
- Dense layer with **Sigmoid** output for real/fake classification

### Training Setup
- **Batch size**: 128  
- **Latent dimension**: 100  
- **Learning rate**: 2e-4  
- **Optimizer**: Adam (β1=0.5)  
- **Loss**: Binary cross-entropy  
- **Epochs**: 1000  


## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/keshav-077/1mage-Generation-using-DCGAN
   ```

2. Download the CelebA dataset from Kaggle and extract into dataset/:
   ```
     dataset/img_align_celeba/
   ```


 3. Open the notebook:
   ```
  Jupyter Notebook "DCGAN-!mage-Generation.ipynb"

   ```


## 📊 Results

### Loss Curves
```
      - Discriminator loss decreases steadily as it learns to classify real vs fake images.
      - Generator loss increases gradually as the generator improves at fooling the discriminator.
```

   <img src="assessts/Screenshot 2025-09-05 174315.png" alt="LOss">
 

 
