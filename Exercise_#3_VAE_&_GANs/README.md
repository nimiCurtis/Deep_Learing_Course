# Exercise Overview

This exercise report focuses on the implementation and analysis of Variational Autoencoder (VAE), Generative Adversarial Network (GAN), and Wasserstein GAN (WGAN) architectures. The theoretical and practical aspects of these models are explored using datasets such as Fashion MNIST. The report presents the comparison of various metrics, including KL divergence, JS divergence, Wasserstein distance, and classification accuracy. Convergence graphs and generated output images are also provided for visual assessment. The results indicate the effectiveness of the models in generating realistic samples and capturing the underlying data distribution.

---

# Practical Part: VAE & GAN

## VAE

### Dataset
The VAE implementation in this exercise utilizes the Fashion MNIST dataset, which consists of grayscale images representing various fashion items. Different amounts of data are used for training the SVM model for each class, specifically: 100, 600, 1000, and 3000 samples.

### Model
The code implements a Variational Autoencoder (VAE) based on the paper "Semi-supervised Learning with Deep Generative Models". Additionally, the SVM model from the scikit-learn library is trained after the VAE.

### Usage
To run this code, follow these steps:
1. Set the appropriate directory paths within the "For the instructor" section according to your directory setup.
2. Run the code cell by cell.
3. Use the flag value of 0 to train both the VAE and the SVM, and 1 to load pre-trained models.
4. Specify the number of samples for each class and run all the cells.

### Results
The results of M1 + SVM are as follows:
- Number of samples: 100 | Accuracy: 79.0%
- Number of samples: 600 | Accuracy: 82.3%
- Number of samples: 1000 | Accuracy: 83.1%
- Number of samples: 3000 | Accuracy: 84.3%


## GAN

### Dataset
The GAN models (DC GAN & WGAN) were trained on the Fashion MNIST dataset, which contains 70,000 grayscale images of fashion items, categorized into 10 classes.

### Model
The code implements a Generative Adversarial Network (GAN) consisting of a Generator and a Discriminator. The Generator generates synthetic images using linear and convolutional transpose layers, while the Discriminator classifies input images as real or fake using convolutional layers with leaky ReLU activation. The loss calculations and optimizer parameters differ for each GAN type.

### Usage
To run this code, follow these steps:
1. Set the appropriate directory paths within the "For the instructor" section according to your directory setup.
2. Run the code cell by cell.
3. Use the "Run training" cell to train both the DCGAN and the WGAN.
4. Use the last two cells under "Display" to infer the saved models.
