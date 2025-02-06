# 🎨 Monet-Style Image Generation using GANs

## 📌 Project Overview
This project explores **Generative Adversarial Networks (GANs)** for transforming ordinary photographs into **Monet-style paintings**. We implement and compare multiple GAN architectures to analyze their effectiveness in artistic style transfer.

## 🏆 Models Implemented
- **CycleGAN** - Leverages cycle consistency loss for high-quality translation.
- **U-GAT-IT** - Uses adaptive layer-instance normalization for better fine-grained style transfer.
- **VAE-GAN** - Combines Variational Autoencoders (VAE) with GANs for structured latent representation.
- **WGAN** - Utilizes Wasserstein distance to stabilize training and improve output diversity.

---

## 🛠️ Technologies & Libraries Used
### **Programming & Frameworks**
- **Python 3.8+**
- **PyTorch** (Primary deep learning framework)
- **Torchvision** (For dataset transformations & augmentation)
- **OpenCV** (For image preprocessing)
- **NumPy & Pandas** (For data handling)
- **Matplotlib & Seaborn** (For visualization)

### **GAN-Specific Implementations**
- **CycleGAN, U-GAT-IT, WGAN, VAE-GAN** implemented using **PyTorch**  
- **CUDA & cuDNN** enabled for GPU acceleration  

### **Tools Used**
- **Jupyter Notebook** (for model development)
- **Google Colab** (for GPU-based training)
- **Weights & Biases (W&B)** (for experiment tracking)

---

## 📂 Dataset Details
- **Source**: [Kaggle - "I'm Something of a Painter Myself"](https://www.kaggle.com/competitions/gan-getting-started/overview)
- **Photos**: 7,038 images
- **Monet Paintings**: 300 images
- **Resolution**: All images resized to **256x256** pixels

### **Data Preprocessing & Augmentation**
- **Normalization**: Converted images to [−1,1] scale.
- **Resizing & Cropping**: All images resized to **256x256** with aspect ratio 1:1.
- **Data Augmentation**:
  - Horizontal & vertical flips
  - Color jittering
  - Gaussian blur for WGAN preprocessing
  - Perspective distortions (for U-GAT-IT)
  - Random cropping (for CycleGAN)

---

## 📈 Evaluation Metrics
- **Fréchet Inception Distance (FID)** - Measures realism of generated images.
- **Memorization-informed FID (MiFID)** - Penalizes overfitting and memorization.
- **Lower MiFID** → Higher quality & diversity.

### **Results**
| Model          | Epochs | MiFID Score (↓) |
|---------------|--------|----------------|
| **CycleGAN**  | 20     | **58.35** |
| **U-GAT-IT**  | 30     | 61.31  |
| **VAE-GAN**   | 15     | 61.97  |
| **WGAN**      | 100    | 80.98  |

✅ **CycleGAN** produced the best results, achieving the lowest **MiFID score** while maintaining training efficiency.

## 🖼️ Sample Outputs
---
<img width="750" alt="Screenshot 2025-02-05 at 11 28 11 PM" src="https://github.com/user-attachments/assets/7f56a5c1-7fe0-4617-861d-c07f997d6c15" />



## 🚀 Future Improvements
- Enhance models with **attention mechanisms** to better capture Monet's brushwork.
- Optimize architectures for **faster training** and **lower computational cost**.
- Implement **style-specific augmentation** for improved artistic realism.

---

## 🔗 References
- [CycleGAN Paper](https://arxiv.org/abs/1703.10593)
- [U-GAT-IT Paper](https://openreview.net/forum?id=BJlZ5ySKPH)
- [WGAN Paper](https://arxiv.org/abs/1701.07875)
- [MiFID Metric Paper](https://doi.org/10.1038/s41524-023-01042-3)

---

## 💡 Contributors
- Dinesh Reddy Kothur
- Harshitha reddy L
- Shivani Reddy B
- Sai Kiran B
- Nikitha G
