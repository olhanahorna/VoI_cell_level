# VoI_cell_level

This repository contains the codebase for the manuscript "Evaluating the value of cell-level information in multi-objective forest planning"

The following files are contained in this directory:

README.md -- brief instructions to run the analysis.

Data folder:
    
    2025-03-27_stands_30_GIT.parquet - input file for optimization that contains data for stands. This file is the output of the forest simulator Gaya 2.0
    
    2025-08-13_cells_30_clustered_GIT_compressed.parquet - input file for optimization that contains data for cells. This file is the output of the forest simulator Gaya 2.0. It also includes additional columns to identify what segment each cells belongs within each cluster. Each cluster is presented as new column. An additional column is added to identify what stand each cells belongs to (stands as cluster case)
    
    grouping_options_4cells.pkl - dictionary with segmentation information to be used in the optimization for the cluster case. 


Python folder:

    2025-03-13_fixing_broken_cells.ipynb - code used to fix the "broken" fragmented cells along stand boundaries. Only needed to be used if the input data does not include uniform cells.

    2025-03-25_segmentation_clusters.ipynb - code used for segmentation and creation of multiple clusters.

    2025-03-26_Optimization_no_cluster.ipynb - code for optimization without inclusion of clusters. Used for optimizing stands and cells as independent management units.

    2025-03-29_Optimization_clusters.ipynb - code for optimization of clusters. The model will define the optimal cluster for a problem to be solved. 

    2025-03-31_optimization_cluster_iterative.ipynb - and an alternative formulation for solving the clusters. In this version, the model will solve each cluster separately and save the outputs. The optimal cluster could be then defined by defining which cluster produced the best objective function. This version of the model could be advantageous to see the distribution of the outputs. 



  
