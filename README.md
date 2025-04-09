# 🔬 Sparse RBM for Gene Expression-Based Cancer Classification

This project uses a **Sparse Restricted Boltzmann Machine (RBM)** for **feature extraction** and a **Random Forest classifier** for classifying gene expression data between **Acute Lymphoblastic Leukemia (ALL)** and **Acute Myeloid Leukemia (AML)**. The dataset contains expression profiles with over 7000 genes across 38 samples.

---

## 📊 Dataset

- **Source**: [Golub et al. (1999)](https://pubmed.ncbi.nlm.nih.gov/10391217/)
- **Samples**: 38
- **Features**: 7129 genes
- **Classes**: 
  - `ALL` – Acute Lymphoblastic Leukemia
  - `AML` – Acute Myeloid Leukemia

---

## 🧠 Model Architecture

1. **Preprocessing**:
   - StandardScaler for normalization
   - PCA for dimensionality reduction

2. **Feature Extraction**:
   - Sparse **BernoulliRBM** with tunable hidden units (e.g., 100)

3. **Classification**:
   - **RandomForestClassifier** with `class_weight='balanced'`

---

## 📈 Results

| Metric          | Value         |
|-----------------|---------------|
| Test Accuracy   | ~83%          |
| Cross-Validation | ~70%          |
| F1-score (ALL)  | 0.90          |
| F1-score (AML)  | 0.50 (class imbalance) |

---

## 🧪 How to Run

### 🔧 Requirements

```bash
pip install numpy pandas scikit-learn imbalanced-learn matplotlib seaborn
