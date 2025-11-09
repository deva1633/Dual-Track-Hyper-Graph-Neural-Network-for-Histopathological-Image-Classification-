# Dual-Track-Hyper-Graph-Neural-Network-for-Histopathological-Image-Classification-
This project introduces a Dual-Track Hypergraph Neural Network (HGNN) combining CNN and Dynamic Weighted HGNN for multi-class classification of lung and colon cancer histopathological images, capturing both fine-grained morphological features and complex tissue-level relationships accurately. Traditional CNN models often fail to capture **non-local dependencies** and **relational tissue structures**, limiting diagnostic accuracy.  

The proposed **Dual-Track HGNN** integrates **Convolutional Neural Networks (CNNs)** with a **Dynamic Weighted Hypergraph Neural Network** to achieve both **fine-grained morphological analysis** and **topological relationship modeling**.

---

## 🚀 Key Features

- **Dual-Track Architecture**
  - **CNN Track:** Extracts local morphological features like cell nuclei and glandular patterns.
  - **Dynamic HGNN Track:** Models high-order and non-local relationships between image regions.
- **Dynamic Edge Weighting:** Learns adaptive connections between tissue components.
- **Feature Fusion Layer:** Merges CNN and HGNN embeddings for robust classification.
- **End-to-End Trainable:** Fully implemented using PyTorch.

---

## 📊 Results

| Model Type | Accuracy | AUC-ROC | Interpretability |
|-------------|-----------|----------|------------------|
| CNN Only | 91.20% | 0.940 | Low |
| CNN + Static Hypergraph | 93.75% | 0.960 | Moderate |
| **Dual-Track CNN–Dynamic HGNN (Proposed)** | **97.20%** | **0.985** | **High** |

---

## 🧠 Architecture Overview

├── CNN Track → Local Feature Extraction
├── HGNN Track → Relational Feature Modeling
└── Feature Fusion → Fully Connected Layer → Output (5 Classes)


---

## 🧾 Dataset

- **Dataset:** [LC25000](https://www.kaggle.com/datasets)  
- **Description:** 25,000+ H&E-stained lung and colon cancer images  
- **Classes:** 5 (Benign Lung, Benign Colon, Adenocarcinoma Lung, Adenocarcinoma Colon, Squamous Cell Carcinoma)  

---

## ⚙️ Implementation Details

- **Framework:** PyTorch  
- **Epochs:** 20 (CNN and HGNN trained separately)  
- **Optimizer:** Adam  
- **Learning Rate:** 0.001  
- **Loss Function:** Cross-Entropy  
- **Batch Size:** 32  

---

## 🧩 Dependencies

Install required packages before training:

```bash
pip install torch torchvision torchaudio
pip install numpy pandas scikit-learn opencv-python
pip install matplotlib seaborn
📁 Dual-Track-HGNN/
├── data/                # Dataset directory
├── models/
│   ├── cnn_model.py
│   ├── hgnn_model.py
│   └── dual_track.py
├── utils/
│   ├── preprocessing.py
│   ├── metrics.py
│   └── visualization.py
├── train_cnn.py
├── train_hgnn.py
├── evaluate.py
└── README.md


