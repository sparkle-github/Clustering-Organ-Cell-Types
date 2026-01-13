# Clustering-Organ-Cell-Types
My project uses the Tabula Sapiens dataset from the Chan Zuckerberg Biohub (CZ Biohub, SF) to cluster scRNA-seq data by gene expression and biological features, identify distinct cell types and states for insights into organ structure and heterogeneity, and validate results using a developed novel cluster validation algorithm.

### Master's Research Project | San Jose State University

## 📌 Project Overview
This project applies unsupervised machine learning techniques to cluster organ cell types based on gene expression data. The goal was to identify distinct cell subpopulations to aid in medical/research application, e.g., early disease detection.

**Key Objectives:**
* Preprocess large-scale biological datasets (~12GB).
* Implement dimensionality reduction (e.g., PCA, t-SNE).
* Apply clustering algorithms (e.g., K-Means) to categorize cell types.
* Visualize clusters for biological interpretation.
* Validate clusters using novel cluster validation algorithm based on Cell Lineage Tree.

## 📓 Code
* **298_k-means_AllCells.ipynb** - Contains All Cells dataset contains over 1.1M cells from 28 organs of 24 human subjects. The dataset is loaded, preprocessed, normalized, mitochondrial genes are removed, and the Elbow method is carried out to identify the number of clusters.
* **298_compare_kmeans_celltype_AllCells.ipynb** - After determining the number of clusters in the above file, k-means in performed on the All Cells data and visualized using data viaualization techniques like PCA, UMAP and t-SNE; original clusters are compared with the generated clusters using heatmaps. 
* **CS298_SampleData_Analysis_5April_2025_Mod20Apr.ipynb** - Here 2 distinct non-overlapping subsets of the All Cells data are extracted based on the top most expressed genes, preprocessed again and the number of clusters are determined and k-means is performed, data is visualized, cluster selection metrics (Shannon's Diversity and Pielou's Evenness) are used to further select few clusters to determine their validity. Clusters are validated using novel Cluster validation algorithms developed based on the Cell Developmental Stage Tree.

**View Notebook Here (via nbviewer)** : https://nbviewer.org/github/sparkle-github/Clustering-Organ-Cell-Types/blob/main/CS298_SampleData_Analysis_5April_2025_Mod20Apr.ipynb
  *(Note: This file is hosted on GitHub but viewed via nbviewer due to large file size)*


## 🛠️ Technologies Used
* **Language:** Python 3.12
* **Libraries:** Scanpy, Anndata, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
* **Tools:** Jupyter Notebook



## ⚠️ Dataset Information
**Note:** The full raw dataset used for this project is approximately **12GB** and is NOT included in this repository due to size limitations.
The official website for Tabula Sapiens by CZ Biohub - https://tabula-sapiens.sf.czbiohub.org/

* **Source:** Tabula Sapiens - https://cellxgene.cziscience.com/collections/e5f58829-1a66-40b5-a624-9046778e74f5 
* **Access:** To run this project locally, please download the All Cells dataset from the source above and follow the steps in the jupyter notebooks


## 📜 License & Citation
This project is open-source under the **MIT License**.

If you use this code or methodology in your research, please cite:
> Swathi M V S. (2025). *Organ Cell Type Clustering*. Master's Project, San Jose State University. Available at: https://github.com/sparkle-github/Clustering-Organ-Cell-Types

## 🙌 Acknowledgements
* Guidance provided by Prof. Chris Pollett.
* Publication - https://www.science.org/doi/10.1126/science.abl4896
* Motivation - https://www.economist.com/science-and-technology/2023/03/08/a-cartography-of-human-histology-is-in-the-making


