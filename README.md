
# UMAP Evaluation on Simulated scRNA-seq Data

This repository contains code and visualizations for evaluating UMAP embeddings on simulated single-cell RNA-seq (scRNA-seq) data generated with [SymSim](https://github.com/YosefLab/SymSim). The goal of this project is to systematically explore how different distance metrics and dropout levels affect UMAP performance in sparse, high-dimensional gene expression data.

## 📁 Folder Overview

All figures and plots are grouped by dataset and analysis type.

### 🔹 `UMAP_S500/`
UMAP embeddings for the **S500 simple** dataset across all dropout levels (0.1–0.9).

- **File:** `UMAP_ALL_S500.ipynb`

### 🔹 `UMAP_S500_O/`
UMAP embeddings for the **S500 complex** dataset (with nested cell subclasses) across all dropout levels.

- **File:** `UMAP_ALL_S500_O.ipynb`

### 🔹 `UMAP_S5000/`
UMAP embeddings for the **S5000 simple** dataset across all dropout levels.

- **File:** `UMAP_ALL_S5000.ipynb`

### 🔹 `UMAP_S10000/`
UMAP embeddings for the **S10000 simple** dataset across all dropout levels.

- **File:** `UMAP_ALL_S10000.ipynb`

### 🔹 `UMAP_S10000_O/`
UMAP embeddings for the **S10000 complex** dataset (with nested cell subclasses) across all dropout levels.

- **File:** `UMAP_ALL_S10000_O.ipynb`
---

## 🖼️ Figures for Paper: Focused UMAP Visualizations

These UMAP plots were used in the final paper/report to highlight specific dropout conditions and metric behavior.

### 🔸 `UMAP_S500_UMAPSFORPAPER_DROPOUT04_06.ipynb`
UMAP embeddings for **S500 simple**, comparing dropout levels 0.4 and 0.6.

### 🔸 `UMAP_S10000_UMAPSFORPAPER_DROPOUT02_0.8.ipynb`
UMAP embeddings for **S10000 simple**, comparing dropout levels 0.2 and 0.8.

### 🔸 `UMAP_S10000C_UMAPSFORPAPER_DROPOUT02_0.8.ipynb`
UMAP embeddings for **S10000 complex**, comparing dropout levels 0.2 and 0.8.

---

## ✅ Baseline UMAPs (No Dropout)

### 🔸 `UMAP_S500.png`
UMAP embedding for **S500 simple**, no dropout applied.

### 🔸 `UMAP_S500C.png`
UMAP embedding for **S500 complex**, no dropout applied.

---

## ⚙️ Code Summary

The Python code used to generate these plots follows a unified pipeline:

- Loads expression matrices and cell-type labels using `scanpy` and `pandas`
- Constructs k-nearest neighbor graphs with `sc.pp.neighbors`
- Applies UMAP (`sc.tl.umap`) using different distance metrics:
  - Euclidean (L2)
  - Manhattan (L1)
  - Minkowski with p=0.5
- Repeats embeddings multiple times to assess stability
- Computes:
  - Trustworthiness (local structure preservation)
  - Silhouette score (cluster separability)
- Results are aggregated and saved for visualization

Refer to the project report or notebook scripts for specific parameter settings and implementation details.

---

## 📌 Notes

- All UMAPs were computed directly on the raw high-dimensional data (no PCA).
- Dropout levels simulate increasing technical sparsity in scRNA-seq.
- Metric evaluation bias was explored and documented.

---

## 📎 Citation

If you use this code or figures, please cite our project report or link back to this repository. Thanks!


