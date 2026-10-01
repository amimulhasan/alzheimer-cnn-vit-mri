# Integrating CNN and ViT for High-Accuracy Alzheimer’s Disease Detection and Staging from MRI

A hybrid deep learning framework combining **Convolutional Neural Networks (CNNs)** and **Vision Transformers (ViTs)** for accurate four-class Alzheimer’s disease classification and staging from MRI images.

**Paper accepted at:** 2026 IEEE 2nd International Conference on Quantum Photonics, Artificial Intelligence, and Networking (QPAIN), Chittagong, Bangladesh.

---

## Model Overview

| Component | Role |
|-----------|------|
| **CNN Branch** | Extracts local texture and fine-grained spatial features |
| **ViT Encoder** | Captures long-range global contextual dependencies via self-attention |
| **Hybrid Fusion** | Concatenates local + global features for robust classification |

### Key Results
- **Peak Accuracy:** 99.97%
- **10-Fold CV Accuracy:** 99.97% (average)
- **Dataset:** 4,400 balanced MRI scans
- **Classes:** Non-Demented, Very Mild Demented, Mild Demented, Moderately Demented

---

## Project Structure

```
├── Integrating_CNN_and_VIT_for_High_Accuracy_Alzheimer_s_Disease_Detection_and_Staging_from_MRI__7_.pdf
├── README.md
├── requirements.txt
└── .gitignore
```

> All figures (Architecture, Accuracy Curve, Confusion Matrix, Grad-CAM etc.) are included inside the PDF paper.

---

## Installation

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME

# Create virtual environment (recommended)
python -m venv venv
source venv/bin/activate          # Linux/Mac
# venv\Scripts\activate           # Windows

# Install dependencies
pip install -r requirements.txt
```

---

## Dataset

The **AD Moderate Dataset** was created by merging:
- OASIS Alzheimer’s Detection Dataset
- Kaggle Medical Scan Classification Dataset

**Class distribution (balanced):**

| Class                  | Total | Train (80%) | Val (10%) | Test (10%) |
|------------------------|-------|-------------|-----------|------------|
| Non-Demented           | 1100  | 880         | 110       | 110        |
| Very Mildly Demented   | 1100  | 880         | 110       | 110        |
| Mildly Demented        | 1100  | 880         | 110       | 110        |
| Moderately Demented    | 1100  | 880         | 110       | 110        |
| **Total**              | **4400** | **3520** | **440** | **440** |

> Dataset files are **not** included. Please download from original sources.

---

## Hyperparameters

| Parameter                    | Value                          |
|------------------------------|--------------------------------|
| Input Image Size             | 224 × 224                      |
| Batch Size                   | 32                             |
| Patch Size                   | 16 × 16                        |
| Number of Patches            | 196                            |
| Projection Dimension         | 64                             |
| Transformer Layers           | 8                              |
| Attention Heads              | 4                              |
| MLP Dimension                | 128                            |
| Epochs                       | 50                             |
| Optimizer                    | Adam                           |
| Learning Rate                | 0.0001                         |
| Loss Function                | Sparse Categorical Crossentropy|
| Number of Classes            | 4                              |

---

## Results Summary

| Metric              | Score    |
|---------------------|----------|
| Test Accuracy       | 99.97%   |
| Precision (Avg)     | 99.98%   |
| Recall (Avg)        | 99.98%   |
| F1-Score (Avg)      | 99.98%   |
| Specificity         | 99.99%   |

### Class-wise Performance

| Class   | Precision | Recall  | F1-score |
|---------|-----------|---------|----------|
| Class 1 | 99.54%    | 98.63%  | 99.08%   |
| Class 2 | 97.22%    | 100.00% | 98.59%   |
| Class 3 | 99.13%    | 99.13%  | 99.13%   |
| Class 4 | 100.00%   | 98.19%  | 99.09%   |

---

## Citation

```bibtex
@inproceedings{rofik2026cnnvit,
  title={Integrating CNN and VIT for High-Accuracy Alzheimer’s Disease Detection and Staging from MRI},
  author={Rofik, Amimul A Hasan and Liva, Ismatul Ferdush and Ali, Md. Yousuf and Islam, Ashikul and Khan, Salman Bin Arif and Hossain, Md. Sabuj},
  booktitle={2026 IEEE 2nd International Conference on Quantum Photonics, Artificial Intelligence, and Networking (QPAIN)},
  year={2026},
  organization={IEEE}
}
```

---

## Authors

- **Amimul A Hasan Rofik** (Corresponding Author) – amimulhasan35@gmail.com  
- Ismatul Ferdush Liva  
- Md. Yousuf Ali  
- Ashikul Islam  
- Salman Bin Arif Khan  
- Md. Sabuj Hossain  

**Affiliation:** Department of Biomedical Engineering, Islamic University, Kushtia-7003, Bangladesh

---

## License

This project is released for research and educational purposes.
