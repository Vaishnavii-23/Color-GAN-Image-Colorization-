#  Colorization of Grayscale Images Using Conditional GANs (cGANs)

Welcome to this image colorization project, where grayscale images get their groove back! Using the power of **Conditional Generative Adversarial Networks (cGANs)**, this project breathes color into black-and-white photos — turning monotone pixels into vibrant visuals 

---

##  Project Overview

> “Color is a power which directly influences the soul.” — Wassily Kandinsky  
This project explores **automatic colorization** of grayscale images using a deep learning model trained on a **small custom dataset**. It leverages the adversarial magic of GANs to generate RGB images from grayscale inputs — sharper and more vivid than traditional pixel-wise techniques.

---

## Aim

To develop a Conditional GAN that colorizes grayscale images into realistic RGB outputs using a high-resolution, visually diverse dataset — without relying on pre-trained networks.

---

## Tech Stack

| Technology     | Purpose                                |
|----------------|----------------------------------------|
| PyTorch        | Deep learning framework for GANs       |
| Torchvision    | Image transformations & datasets       |
| PIL            | Image conversion                       |
| NumPy          | Array operations                       |
| Matplotlib     | Visualization                          |
| Google Colab   | GPU-accelerated training               |

---

##  Model Architecture

### Generator (U-Net)
- Converts grayscale image (1 channel) → color image (3 channels)
- Uses skip connections to preserve spatial info

###  Discriminator (PatchGAN)
- Sees input as a pair (gray + color)
- Trains to tell real from fake colorization

---

##  Workflow

1. Load 10 high-res images
2. Convert them to grayscale
3. Resize to 64x64 and normalize to [-1, 1]
4. Train using:
   - Binary Cross Entropy (GAN loss)
   - L1 loss (pixel-wise similarity)
5. Visualize outputs after each epoch
6. Save final model weights

---

##  Dataset Structure

dataset/
├── color/
│ ├── image1.jpg
│ └── ...
└── grayscale/
├── image1.jpg
└── ...
>  Only 10 images used to simulate a low-data setup.

---

##  Getting Started

### Installation

```bash
git clone https://github.com/yourusername/cgan-image-colorization.git
cd cgan-image-colorization
pip install -r requirements.txt

▶️ Run the Notebook
Launch notebooks/cgan_colorization.ipynb in Google Colab and you're good to go!
