# 🌌 SAR to EO Image Translation using CycleGAN

**Project 1 – Summer School on Deep Dive in Deep Learning**  
**Team Members:**  
- Bhavesh Bhardwaj  
- Satyendra  

---

## 📌 Introduction

This project demonstrates the application of **Cycle-Consistent Generative Adversarial Networks (CycleGANs)** for translating **Synthetic Aperture Radar (SAR)** images into **Electro-Optical (EO)** images. This is particularly useful in scenarios where EO data is obscured or unavailable, such as during cloud cover.

The implementation is based on the **SEN12MS-Subset** dataset (Winter scenes). It includes data preprocessing, CycleGAN model architecture, training, evaluation using SSIM/PSNR, and visualization.

---

## 🗂 Folder Structure

```
.
├── __results___files/         # Output files and logs
├── checkpoints/               # Checkpointed model weights during training
├── final_model_rgb.pth.pth    # Final trained model on RGB configuration
├── generated_samples/         # Visual samples of SAR to EO translations
├── main.ipynb                 # Jupyter notebook to run the project
├── README.md                  # Project documentation
├── Report(README).pdf         # Formal project report
├── requirements.txt           # Required Python packages
```

---

## 🛠️ How to Use

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/sar-to-eo-cycleGAN.git
cd sar-to-eo-cycleGAN
```

### 2. Install Requirements

```bash
pip install -r requirements.txt
```

> Note: You may need to install packages like `rasterio`, `scikit-image`, `torch`, `torchvision`, etc.

### 3. Dataset Setup

Download the SEN12MS-Subset dataset from:  
🔗 [https://mediatum.ub.tum.de/1524895](https://mediatum.ub.tum.de/1524895)

Place the dataset under the following structure:
```
/kaggle/input/sen12ms-subset/sen12ms-subset/
```

Or modify the data path in `main.ipynb` accordingly.

### 4. Run Training Notebook

You can run the notebook in:
- Jupyter
- Colab
- Kaggle

Configure:
```python
band_config = "rgb"
num_epochs = 40
batch_size = 4
```

Start training and monitor the outputs in checkpoints and logs.

---

## 📏 Evaluation Metrics

- **SSIM** (Structural Similarity Index)
- **PSNR** (Peak Signal-to-Noise Ratio)
- Optional: **NDVI** if using NIR bands

---

## 📊 Visualization

- `generated_samples/` contains SAR → EO image comparisons
- Loss trends plotted inside the notebook

---

## ✅ Summary of Results (RGB Config)

- SSIM: `0.4962 ± 0.0821`
- PSNR: `17.9358 ± 3.9486`

---

## 📌 Future Enhancements

- Identity loss usage
- NDVI-based evaluation
- Other seasonal or geographic datasets
- Advanced GAN architectures (e.g., Attention GAN)

---

## 📄 License

This work is for academic and research purposes only under the summer school project guidelines.

---

## 🙏 Acknowledgments

- **SEN12MS dataset** contributors
- **CycleGAN original authors**
- Organizers of **Deep Dive in Deep Learning** Summer School

---
