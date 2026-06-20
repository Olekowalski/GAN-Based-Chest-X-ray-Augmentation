# GAN-Augmented Chest X-ray Classification

## Overview

This project investigates the use of Generative Adversarial Networks (GANs) for balancing imbalanced Chest X-ray datasets and improving image classification performance.

A conditional WGAN-GP model was trained to generate synthetic Chest X-ray images for underrepresented classes. The generated images were subsequently used to augment the training dataset and evaluate their impact on classification accuracy.

---

## Dataset

Chest X-ray dataset containing four classes with the following distribution:

| Class   | Number of images |
| ------- | ---------------- |
| Class 0 | 460              |
| Class 1 | 1341             |
| Class 2 | 3875             |
| Class 3 | 650              |

To reduce computational cost during GAN training, the largest class was excluded.

---

### Image generation

Conditional **WGAN-GP**

Training configuration:

* Resolution: 128×128
* Latent dimension: 128
* Batch size: 16
* Epochs: 500


### GAN augmentation

Synthetic images were generated for minority classes and added to the training set in order to reduce class imbalance.

Performance was evaluated using:

* Accuracy
* Precision
* Recall
* F1-score




* Additional experiments on class balancing strategies
* Comparison of attention maps between real and synthetic images
