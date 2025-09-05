DCGAN Implementation

This repository contains an implementation of a Deep Convolutional Generative Adversarial Network (DCGAN). The project demonstrates how GANs can learn to generate realistic-looking images from random noise.

📌 Project Overview

Built using PyTorch

Implements Generator and Discriminator networks with convolutional layers

Trains adversarially to generate synthetic images

Evaluates performance through visualization of generated samples and loss plots

📂 Dataset

The model was trained on the  CelebA.

Number of classes: 5864 files belonging to 1 classes.

Image size: 64×64 greyscale 




⚙️ Requirements
```
pip install torch torchvision numpy matplotlib jupyter
```

🏃 How to Run

Clone the repository:

```

git clone https://github.com/your-username/dcgan-implementation.git
cd dcgan-implementation
```


Open the notebook:
```

Jupyter Notebook "2-DCGAN By Neuralearn.ai-.ipynb"

```


Run all cells to train the DCGAN and generate images.

📊 Results
Training Progress

Discriminator Loss: decreases steadily, stabilizing after ~[X] epochs

Generator Loss: shows adversarial training dynamics, stabilizing after ~[X] epochs

Sample Outputs

Generated images at different training stages:

Epoch 1	Epoch 25	Epoch 50	Epoch 100

	
	
	

(Add your generated sample images from the notebook here.)

Observations

Early epochs produce noisy images with little structure

Mid-training shows clearer shapes resembling dataset images

Later epochs generate sharper, more realistic images

📖 References

Radford et al., "Unsupervised Representation Learning with Deep Convolutional GANs"

PyTorch DCGAN Tutorial
