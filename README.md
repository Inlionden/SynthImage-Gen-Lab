# 🎨 Realistic Face Generation using DCGAN

This project demonstrates how to build and train a **Deep Convolutional Generative Adversarial Network (DCGAN)** to generate realistic human face images using the **CelebA dataset**.

📁 **Notebook**: [`image-generation.ipynb`](./notebooks/image-generation.ipynb)

---

## 🚀 Project Highlights

- 🧠 Uses a **GAN architecture** with convolutional layers for stable image generation.
- 🧰 Implemented using **PyTorch** for full flexibility and GPU acceleration.
- 📊 Trains on the **CelebA** dataset of celebrity faces.
- 🧪 Includes training visualization: loss plots and generated image grids.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Model Architecture](#-model-architecture)
- [Dataset](#-dataset)
- [How to Run](#-how-to-run)
- [Results](#-results)
- [Tips for Improvement](#-tips-for-improvement)
- [References](#-references)

---

## 📖 Project Overview

Generative Adversarial Networks (GANs) consist of two models:
- **Generator**: Learns to produce fake images that resemble the real data.
- **Discriminator**: Learns to distinguish between real and generated images.

They are trained simultaneously in a zero-sum game. Over time, the generator becomes better at fooling the discriminator, and produces realistic outputs.

---

## 🧱 Model Architecture

### Generator

- Input: 100-dim noise vector
- Transposed convolution layers to upsample
- BatchNorm and ReLU activations
- Output: 3×64×64 RGB image

### Discriminator

- Input: 3×64×64 RGB image
- Convolutional layers to downsample
- LeakyReLU and dropout
- Output: Single probability (real/fake)

---

## 🖼️ Dataset

- **CelebA (CelebFaces Attributes Dataset)**  
- Contains over 200,000 celebrity face images
- Automatically downloaded and loaded in PyTorch `Dataset` class

---

## 🛠️ How to Run

1. 📦 Install dependencies:

```bash
pip install torch torchvision matplotlib

# auto-commit
