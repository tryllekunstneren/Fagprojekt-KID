
# UMAP Evaluation on Simulated scRNA-seq Data

This repository contains code and visualizations for evaluating UMAP embeddings on simulated single-cell RNA-seq (scRNA-seq) data generated with [SymSim](https://github.com/YosefLab/SymSim). The goal of this project is to systematically explore how different distance metrics and dropout levels affect UMAP performance in sparse, high-dimensional gene expression data.

## 🔁 Version Control and Reproducibility

This project was developed and tested using **Python 3.11.5** and the latest available versions (as of runtime) of the following libraries:

- `numpy`
- `pandas`
- `scanpy`
- `scikit-learn`
- `scipy`
- `pickle` (Python built-in)

To ensure reproducibility, we recommend creating a virtual environment and using:

bash
pip freeze > requirements.txt

# 📁 Data Access

The datasets used in this project are stored externally due to their size.

You can access and download all datasets here:

🔗 [Google Drive – UMAP scRNA-seq Data](https://drive.google.com/drive/folders/1JDoNXzZA_zlaCrL6FRGtp7H4gGrwB3-E?usp=sharing)

After downloading, place the datasets into a `data/` folder at the root of this project with the following structure:
data/

├── S500/

├── S5000/

└── S10000/

This structure is expected by the notebooks in this repository. Make sure to maintain the folder names.


## 📁 Folder Overview

All figures, notebooks, and plots are grouped by dataset and analysis type.

---

### 🔹 UMAP_S500/

Contains all UMAP and evaluation plots for the **S500 simple** and **S500 complex** datasets.

#### Files:
- `UMAP_ALL_S500.ipynb`  
  UMAP embeddings for **S500 simple** across all dropout levels (0.1–0.9).
  
- `UMAP_ALL_S500_O.ipynb`  
  UMAP embeddings for **S500 complex** (nested subclasses) across all dropout levels.

- `UMAP_S500_UMAPSFORPAPER_DROPOUT04_06.ipynb`  
  Focused UMAP visualizations of **S500 simple** at dropout 0.4 and 0.6 for the paper.

- `UMAP_S500.ipynb`  
  UMAP visualizations for the **S500 simple** dataset with no dropout.

- `UMAP_S500C.ipynb`  
  UMAP visualizations for the **S500 complex** dataset with no dropout.

#### Evaluation Metric Sensitivity (S500 only):

- `UMAP_EVALMETRICS_EUCLIDEAN_S500.ipynb`  
- `UMAP_EVALMETRICS_MANHATTAN_S500.ipynb`  
- `UMAP_EVALMETRICS_MINKOWSKI_S500.ipynb`  

---

### 🔹 UMAP_S5000/

Contains UMAP visualizations for the **S5000 simple** dataset.

#### Files:
- `UMAP_ALL_S5000.ipynb`  
  UMAP embeddings across all dropout levels (0.1–0.9).

---

### 🔹 UMAP_S10000/

Contains UMAP analyses for the **S10000 simple** and **S10000 complex** datasets.

#### Files:
- `UMAP_ALL_S10000.ipynb`  
  UMAP embeddings for **S10000 simple** across all dropout levels.

- `UMAP_ALL_S10000_O.ipynb`  
  UMAP embeddings for **S10000 complex** (nested classes) across all dropout levels.

- `UMAP_S10000_UMAPSFORPAPER_DROPOUT02_0.8.ipynb`  
  Focused UMAP visualizations of **S10000 simple** at dropout 0.2 and 0.8 for the paper.

- `UMAP_S10000C_UMAPSFORPAPER_DROPOUT02_0.8.ipynb`  
  UMAP visualizations for **S10000 complex** at dropout 0.2 and 0.8 for visual comparison.

---

## 📎 Citation

If you use this code or figures, please cite our project report or link back to this repository. Thanks!


