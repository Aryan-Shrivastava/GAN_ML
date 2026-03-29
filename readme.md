---

#  GANs Image Generation Project

A deep learning project that leverages **Generative Adversarial Networks (GANs)** to generate realistic synthetic images of handwritten digits and anime-style faces.

---

##  Project Highlights

* Generate **MNIST-like handwritten digits**
* Create **anime-style faces** using GANs
* Built using **PyTorch**
* Modular and extensible codebase

---

##  What are GANs?

Generative Adversarial Networks consist of two competing neural networks:

* **Generator (G)**
  Learns to create realistic images from random noise

* **Discriminator (D)**
  Learns to distinguish between real and fake images

They are trained in a **minimax game**, where:

* Generator tries to fool the discriminator
* Discriminator tries not to be fooled

---

##  Architecture Overview

```
Noise (z) ───▶ Generator ───▶ Fake Image
                          │
Real Image ───────────────┘
                          ▼
                    Discriminator ───▶ Real / Fake
```

---

##  Datasets Used

### 1. MNIST Dataset

* 28x28 grayscale images of handwritten digits (0–9)
* Automatically downloaded via `torchvision`

### 2. Anime Face Dataset

* RGB images of anime characters
* Can use:

  * Kaggle Anime Faces dataset
  * Custom scraped dataset

---

##  Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/your-username/gan-image-generation.git
cd gan-image-generation

pip install torch torchvision matplotlib
```

---

##  How to Run

###  Train on MNIST Digits

```bash
python gan_digit.py
```

###  Train on Anime Faces

```bash
python gan_anime.py
```

---

##  Generate Images

```python
import torch

noise = torch.randn(batch_size, noise_dim)
fake_images = generator(noise)
```

---

##  Project Structure

```
├── gan_digit.py        # GAN training for MNIST
├── gan_anime.py        # GAN training for anime faces
├── models.py           # Generator & Discriminator architectures
├── utils.py            # Data loading & preprocessing utilities
├── outputs/            # Generated images
└── README.md
```

---

##  Results

###  Generated Digits

* Realistic handwritten digits resembling MNIST samples

###  Generated Anime Faces

* Visually appealing anime-style faces
* Improved quality with longer training and tuning

---

##  Evaluation

* Visual inspection of generated samples
* Loss curves for Generator and Discriminator
* (Optional) Metrics:

  * FID Score (Fréchet Inception Distance)
  * IS (Inception Score)

---

##  Future Improvements

* Implement advanced architectures:

  * DCGAN
  * WGAN / WGAN-GP
* Add training visualization (TensorBoard)
* Improve dataset diversity
* Hyperparameter tuning
* Conditional GAN (cGAN)

---

##  Key Learnings

* Stability challenges in GAN training
* Importance of balance between Generator & Discriminator
* Effect of architecture and hyperparameters on output quality

---

##  License

This project is licensed under the **MIT License**.

---

##  Contributing

Contributions are welcome! Feel free to fork the repo and submit a PR.

---
