# 🧬 AI-enhanced Raman Spectroscopy for Early Detection of Skin Cancer

This project explores a lightweight yet powerful deep learning model for early-stage skin cancer detection using Raman spectroscopy. The core architecture is a **Single-Layer Multiple-Kernel Convolutional Neural Network (SLMK-CNN)**, developed to simultaneously enable **classification** and **histological interpretation** of biological spectra without heavy preprocessing.

> 🧪 Reference: Sohn WB, Lee SY, Kim S. “Single-layer multiple-kernel-based convolutional neural network for biological Raman spectral analysis.” *Journal of Raman Spectroscopy*, 51(3), 2020. [https://doi.org/10.1002/jrs.5804](https://doi.org/10.1002/jrs.5804)

---

## 🔍 Project Summary

- **Goal**: Classify UV-induced skin damage using Raman spectra from porcine samples.
- **Challenge**: Raw Raman signals are often noisy, and interpretation can be lost in deeper CNNs.
- **Solution**: SLMK-CNN with five parallel convolutional kernels of varying sizes (1×3 to 1×45) to capture multiple spectral characteristics.
- **Key Advantage**: Preserves molecular information (DNA, cholesterol, p53) while achieving high accuracy.

---

## 📊 Dataset

- **Samples**: Porcine skin exposed to UV light for 0, 10, and 24 hours.
- **Spectra**: 360 Raman spectra (120 per group).
- **Measured Range**: 600–1800 cm⁻¹.

![Dataset Overview](./Paper/Figure_Dataset.png)

---

## 🧠 Model Architecture

- Single convolutional layer with **5 parallel kernel sizes**: 1×3, 1×7, 1×13, 1×27, and 1×45.
- Followed by:
  - ReLU activation
  - Flattening layer
  - Fully connected layers (ReLU → Softmax)

![Model Architecture](./Paper/Figure_Model.png)

---

## 🥇 Results

| Input Type    | Model              | Accuracy |
|---------------|--------------------|----------|
| Raw Data      | SLMK-CNN           | 92.5%    |
| Raw Data      | Single-kernel CNN  | 83.3%    |
| Preprocessed  | SLMK-CNN           | 96.4%    |
| Preprocessed  | Single-kernel CNN  | 91.4%    |

- Demonstrated superiority over traditional PC-LDA and single-kernel CNNs.

---

## 🧬 Histological Markers Detected

| Wavenumber (cm⁻¹) | Biomolecule   | Interpretation                   |
|-------------------|----------------|----------------------------------|
| 814               | DNA            | Decrease = DNA damage            |
| 1080              | p53 protein    | Increase = DNA damage response   |
| 1447              | Cholesterol    | Decrease = lipid degradation     |

![Histological Markers](./Paper/Figure_Histology.png)

---

## 🚧 Code

> 🚧 *The code for data preprocessing, model training, and evaluation will be updated soon. Please stay tuned!*

---

## 📄 Citation

Sohn, WB., Lee, SY., and Kim, S., “Single-layer multiple-kernel-based convolutional neural network for biological Raman spectral analysis”, *Journal of Raman Spectroscopy*, 51(3), 2020. [https://doi.org/10.1002/jrs.5804](https://doi.org/10.1002/jrs.5804)

---

## 📬 Contact

For questions or collaboration inquiries:  
**Wonbum Sohn**  
📧 sohnwb@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/wonbumsohn)  
🌐 [www.sohnwb.com](https://www.sohnwb.com)
