# Sparse_RBM
Implementing the Sparse RBM for gene selection and classification

# 🧬 Gene Classification using Sparse Restricted Boltzmann Machine (RBM)

This project implements a Sparse Restricted Boltzmann Machine (RBM) for the classification of leukemia types — Acute Lymphoblastic Leukemia (ALL) and Acute Myeloid Leukemia (AML) — using gene expression data.

---

## 📁 Dataset

We use the **ALL/AML Leukemia Gene Expression Dataset**, available on [Kaggle](https://www.kaggle.com/datasets/andradaolteanu/allaml-leukemia-gene-expression) and originally from the [GEO Database (GSE13159)](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE13159).

### 🔹 Files Used:

- `data_set_ALL_AML_train.csv` — Gene expression values for training samples
- `data_set_ALL_AML_independent.csv` — Gene expression values for independent test samples
- `actual.csv` — Contains the true labels (ALL / AML) for each patient sample

### 🔹 Dataset Summary:

| Detail            | Value     |
|------------------|-----------|
| Total Samples     | 72        |
| Features (Genes)  | ~7000     |
| Classes           | ALL, AML  |
| ALL Samples       | 47        |
| AML Samples       | 25        |

---

## 🧪 Preprocessing

1. **Merge Train and Test Sets:** Combined gene expression data into a single DataFrame.
2. **Transpose:** Ensured each row represents a patient, and each column a gene.
3. **Label Mapping:** Added cancer type labels from `actual.csv`.
4. **Encoding:** Used `LabelEncoder` to convert `ALL` / `AML` into 1 / 0.
5. **Normalization:** Applied `StandardScaler` to normalize all gene expression values to zero mean and unit variance.

---

