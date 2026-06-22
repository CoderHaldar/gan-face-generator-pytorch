# 🎭 CelebA Face Generation using GAN

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red)
![GPU](https://img.shields.io/badge/GPU-RTX%203050-green)
![Dataset](https://img.shields.io/badge/Dataset-CelebA-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview

This project implements a **Generative Adversarial Network (GAN)** using **PyTorch** to generate realistic human face images from random noise vectors.

The model is trained on the **CelebA Dataset**, containing over **200,000 celebrity face images**.

The objective is to learn the underlying distribution of face images and generate new realistic faces that do not exist in the original dataset.

---

## 🧠 What is a GAN?

A GAN consists of two neural networks:

### Generator
- Takes random noise as input
- Generates fake face images

### Discriminator
- Distinguishes between real and generated images
- Learns to identify fake images

Both networks compete against each other, improving over time.

---

## 📂 Dataset

**CelebA (CelebFaces Attributes Dataset)**

- Total Images: 202,599
- Image Size: 64 × 64
- RGB Images

Dataset Link:
https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html

---

## 🏗️ Architecture

### Generator

Input:
- 100-dimensional random noise vector

Layers:
- Linear(100 → 256)
- ReLU
- Linear(256 → 512)
- ReLU
- Linear(512 → 1024)
- ReLU
- Linear(1024 → 12288)
- Tanh

Output:
- 64×64 RGB Image

---

### Discriminator

Input:
- 64×64 RGB Image

Layers:
- Flatten
- Linear
- LeakyReLU
- Linear
- LeakyReLU
- Linear
- LeakyReLU
- Linear
- Sigmoid

Output:
- Probability of image being real

---

## ⚙️ Training Configuration

| Parameter | Value |
|------------|--------|
| Epochs | 10 |
| Batch Size | 128 |
| Learning Rate | 0.0002 |
| Optimizer | Adam |
| Loss Function | Binary Cross Entropy |
| Latent Dimension | 100 |
| Framework | PyTorch |
| GPU | RTX 3050 6GB |

---

## 📁 Project Structure

celeba-face-generation-gan/

├── notebooks/

│ └── GAN_CelebA.ipynb

├── outputs/

│ ├── epoch_1.png

│ ├── epoch_5.png

│ └── epoch_10.png

├── requirements.txt

├── README.md

└── LICENSE

---

## 📈 Training Results

### Generated Images After Training

Insert your generated image outputs here.

Example:

![Epoch10](outputs/epoch_10.png)

---

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/CoderHaldar/celeba-face-generation-gan.git
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run Jupyter Notebook:

```bash
jupyter notebook
```

---

## 🔮 Future Improvements

- Implement DCGAN Architecture
- Add Convolutional Layers
- Save Model Checkpoints
- Train for More Epochs
- Generate Higher Resolution Images
- Add FID Score Evaluation

---

## 👨‍💻 Author

Anurag Haldar

B.Tech CSE | AI/ML Enthusiast

GitHub:
https://github.com/CoderHaldar
