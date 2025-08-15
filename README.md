# VoI_cell_level

This repository contains the codebase for the manuscript:  
**"Evaluating the Value of Cell-Level Information in Multi-Objective Forest Planning"**

---

## Repository Structure

### 📄 README
- **README.md** — Brief instructions to run the analysis.

### 📂 Data
- **2025-03-27_stands_30_GIT.parquet**  
  Input file for optimization containing stand-level data.  
  - This is the output file from the forest simulator **Gaya 2.0**.

- **2025-08-13_cells_30_clustered_GIT_compressed.parquet**  
  Input file for optimization containing cell-level data.  
  - This is the output file from the forest simulator **Gaya 2.0**.  
  - Includes additional columns for segmentation information:  
    - Each cluster is presented as a separate column.  
    - An additional column identifies which stand each cell belongs to (stand as cluster case).  

- **grouping_options_4cells.pkl**  
  Dictionary with segmentation information used in optimization for the cluster case.

### 📂 Python
- **2025-03-13_fixing_broken_cells.ipynb**  
  Code to fix fragmented ("broken") cells along stand boundaries.  
  - Only required if input data does not already include uniform cells.

- **2025-03-25_segmentation_clusters.ipynb**  
  Code for segmentation and creation of multiple clusters.

- **2025-03-26_Optimization_no_cluster.ipynb**  
  Optimization model **without clusters**.  
  - Used for treating stands and cells as independent management units.

- **2025-03-29_Optimization_clusters.ipynb**  
  Optimization model **with clusters**.  
  - The model determines the optimal cluster for the given problem.

- **2025-03-31_optimization_cluster_iterative.ipynb**  
  Alternative cluster optimization formulation.  
  - Solves each cluster separately and saves outputs.  
  - The optimal cluster could then be determined by comparing resulting objective function values.  
  - Advantage: enables exploration of output distributions across clusters.

---





  
