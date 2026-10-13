# Advanced CNNs and Transfer Learning in a Small-Data Regime

This project explores image classification using Convolutional Neural Networks (CNNs) and transfer learning on a selected subset of the Oxford-IIIT Pet dataset. The experiment focuses on classifying images into 10 selected cat and dog breeds and comparing different model training strategies.

## 📂 Repository Structure

Based on the project directory:

```text
├── Bagian A - Analisis Koonseptual.pdf        # Theoretical & conceptual analysis report
├── Bagian_B.ipynb                             # Main Jupyter notebook (training pipeline & evaluation)
├── Bagian_C.pdf                               # In-depth analytical report, comparative findings, & engineering recommendations
├── Grafik Kurva Training B1.png               # Training Loss vs. Validation Loss comparative graph for B1
├── Grafik Kurva Training B2.png               # Training Loss vs. Validation Loss comparative graph for B2
├── Grafik Kurva Training B3.png               # Training Loss vs. Validation Loss comparative graph for B3
├── Failure Analysis.png                       # Several Examples of False Prediction of some data
├── requirements.txt                           # Python package dependencies
└── README.md                                  # Project documentation and setup guide
```
---

## 📊 Summary of Experimental Results

| Code | Setup | Trainable Parameters | Stop Epoch | Test Accuracy | Test Macro F1 |
| :--- | :--- | :---: | :---: | :---: | :---: |
| **B1** | ResNet-18 (Scratch) | 11,181,642 | 20 | 54.36% | 0.526036 | 
| **B2** | ResNet-18 (Feature Extraction) | 5,130 | 17 | 91.28% | 0.913205 | 
| **B3** | ResNet-18 (Progressive Fine-Tuning) | 8,398,858 | 11 | 93.62% | 0.936216 | 
| **B4** | ResNet-18 (B3 w/o Augmentation) | 8,398,858 | 8 | 93.29% | 0.933086 | 
| **B5** | EfficientNet-B0 (Progressive) | 12810 | 20 | 90.94% | 0.909507 |

---

## 🛠️ Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Ws995566/Transfer-Learning-Deep-Learning
   ```

2. **Set up a virtual environment (recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install required dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

---

## 🚀 Reproduction Guide

1. Launch Jupyter Notebook or upload `Bagian B.ipynb` to [Google Colab](https://colab.research.google.com/):
   ```bash
   jupyter notebook Bagian B.ipynb
   ```
2. Make sure a GPU accelerator (e.g., NVIDIA T4 or higher) is enabled.
3. Run cells sequentially. The Oxford-IIIT Pet dataset will automatically download via `torchvision.datasets`.
4. Outputs, metrics, and logs will be populated and exported to `experiment_summary.csv`.
