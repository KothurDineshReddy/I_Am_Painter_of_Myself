# 🎨 Monet-Style Image Generation using GANs

## 📌 Project Overview
This project explores **Generative Adversarial Networks (GANs)** for transforming ordinary photographs into **Monet-style paintings**. We implement and compare multiple GAN architectures to analyze their effectiveness in artistic style transfer.

## 🏆 Models Implemented
- **CycleGAN** - Leverages cycle consistency loss for high-quality translation.
- **U-GAT-IT** - Uses adaptive layer-instance normalization for better fine-grained style transfer.
- **VAE-GAN** - Combines Variational Autoencoders (VAE) with GANs for structured latent representation.
- **WGAN** - Utilizes Wasserstein distance to stabilize training and improve output diversity.

## 📂 Dataset
- **Source**: [Kaggle - "I'm Something of a Painter Myself"](https://www.kaggle.com/competitions/gan-getting-started/overview)
- **Photos**: 7,038 images
- **Monet Paintings**: 300 images
- **Resolution**: All images resized to **256x256** pixels

## 📊 Data Preprocessing & Transformation
- **Normalization**: All images converted to [−1,1] scale.
- **Augmentation**: Random cropping, flipping, color jittering, Gaussian blurring.
- **Aspect Ratio**: Maintained 1:1 for consistency.

## 📈 Evaluation Metrics
- **Fréchet Inception Distance (FID)** - Measures realism of generated images.
- **Memorization-informed FID (MiFID)** - Penalizes overfitting and memorization.
- **Lower MiFID** → Higher quality & diversity.

## 🔍 Results
| Model          | Epochs | MiFID Score (↓) |
|---------------|--------|----------------|
| **CycleGAN**  | 20     | **58.35** |
| **U-GAT-IT**  | 30     | 61.31  |
| **VAE-GAN**   | 15     | 61.97  |
| **WGAN**      | 100    | 80.98  |

✅ **CycleGAN** produced the best results, achieving the lowest **MiFID score** while maintaining training efficiency.

## 🖼️ Sample Outputs
![Generated Monet Style Images](./path_to_your_image.png)  
📌 *Replace `path_to_your_image.png` with the actual image path in your repository.*

## 🚀 Future Improvements
- Enhance models with **attention mechanisms** to better capture Monet's brushwork.
- Optimize architectures for **faster training** and **lower computational cost**.
- Implement **style-specific augmentation** for improved artistic realism.

## 🔗 References
- [CycleGAN Paper](https://arxiv.org/abs/1703.10593)
- [U-GAT-IT Paper](https://openreview.net/forum?id=BJlZ5ySKPH)
- [WGAN Paper](https://arxiv.org/abs/1701.07875)
- [MiFID Metric Paper](https://doi.org/10.1038/s41524-023-01042-3)

## 💡 Contributors

- Dinesh Reddy Kothur
- Harshitha reddy
- Shivani Reddy
- Sai Kiran B
- Nikitha
  
# Run the Jupyter Notebook
jupyter notebook
