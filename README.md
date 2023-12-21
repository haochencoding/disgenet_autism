# Introduction

This repository hosts Hao Chen's coursework for LPI Data Science module 2023-2024. The project entails an analysis of disease-to-disease network and disease-to-gene network to compare syndromic and non-syndromic autism. It used gene-disease association data collected from the DisGeNet database. 

The analysis result is summarised in a final slide presentation, stored in the `presentation` folder. The data analysis python notebook is stored in the `notebook` folder. 

# Data Analysis Logic
For a quick introduction to each notebook, please see below: 
- `0_autism_terms.ipynb`: select autism disorder diagnosis id, result stored in `notebook/processed_data/autism_terms.csv`
- `1_group_autism_subtypes.ipynb`: reprocess raw data by regrouping autism diagnosis according to subtypes, processed data stored in `notebook/processed_data/curated_gene_disease_associations_autism_grouped.csv`
- `2_compare_gene_properties.ipynb`: compare gene properties for autism subtypes
- `3_create_nodes_edges_grouped.Rmd`: hyper-geometric test for the p-value of disease-to-disease association, and create nodes and edges for network analysis:
    - Edge data: `notebook/processed_data/edges_shared_genes_AutismGrouped.csv`
    - Node data: `notebook/processed_data/nodes_diseases_AutismGrouped.csv`
- `4_create_network.ipynb`: create disease-to-disease network:
    - Network for all diseases, stored in `notebook/graphml/p3_network_all_diseases.graphml`
    - Network for autism and neighbour diseases, stored in `notebook/graphml/p3_network_autism_neighbors.graphml`
- `5_centrality_analysis_original.ipynb`: analysis of centrality measurement of disease nodes
- `6_bipartie_autism.ipynb`: create disease-to-gene network for autism genes and autism subtypes
- `7_bipartie_alldisease.ipynb`: create disease-to-gene network for all diseases and related genes
- `8_autism_disease_class.ipynb`: analysis of disease-to-class network

# Data visualization
All data visualization figures and output are stored in `figures` folder:
- The `figures/gene_properties` folder contains figures for gene comparison, the code for generating these figures is contained in `notebook/2_compare_gene_properties.ipynb`
- The `figures/network` folder contains figures for network visualisation, which was conducted using Gephi. The Gephi files and network data is stored in the `notebook/graphml` folder. 