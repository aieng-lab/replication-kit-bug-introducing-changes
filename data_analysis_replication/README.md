# Getting Started

Overall prerequisites:
> 1. Complete data collection
> 2. Copy coded dataset folder, `all_information.csv`, `associated_variables.csv`, `relation_overview.csv`, and `variables overview.csv` into `/input`

## Create Tables for assigning Groups

The script for creating the group assignment tables is [create_tables_group_assignment.ipynb](/create_tables_group_assignment.ipynb). It creates the following output:

1. Nominal pairs (cross tabulation and Firsher's exact test)
    - `relation_overview_fisher.xlsx` in `/output/group_assignment`
2. Nominal/Numeric pairs (boxplots)
    - `relation_overview_boxplots.xlsx` in `/output/group_assignment`
    - Boxplots (PDFs) in `/output/group_assignment/figures`
3. Numeric pairs (Spearman's Rho)
    - `relation_overview_spearmanr.xlsx` in `/output/group_assignment`
4. Zip file of all outputs, timestamped

## Create Network Graphs

The script for creating the network graphs used in the paper is [create_figures_network_graph.ipynb](/create_figures_network_graph.ipynb). It creates the following output:

1. Interactive Graph (pyvis)
    - `network_graph.html` in `/output/results`
2. PDFs for group G2 and G3
    - `network_graph_group_2.pdf` in `/output/results`
    - `network_graph_group_3.pdf` in `/output/results`

## Create other Diagrams and Tables

### Associated Variables

Script: [create_figures_associated_variables.ipynb](/create_figures_associated_variables.ipynb)  
Output (`/output/results`):
 - `association_g2_relations_heatmap.pdf`
 - `association_g3_relations_heatmap.pdf`
 - `association_g2_relations_heatmap_ghafari.pdf`
 - `association_g3_relations_heatmap_ghafari.pdf`
 - `association_g2_relations_heatmap_kononenko.pdf`
 - `association_g3_relations_heatmap_kononenko.pdf`
 - `association_g2_relations_heatmap_querel.pdf`
 - `association_g3_relations_heatmap_querel.pdf`

### Group Distributions

Script: [create_figures_group_distribution.ipynb](/create_figures_group_distribution.ipynb)  
Output (`/output/results`):
  - `group_distribution_grouped.pdf`
  - `group_distribution.pdf`

### Data Distribution

Script: [/create_tables_data_distribution.ipynb](/create_tables_data_distribution.ipynb)  
Output (`/output/results`):
 - `data_distribution_tables.tex`

### Limitations Distribution

Script: [/create_tables_limitations_distribution.ipynb](/create_tables_limitations_distribution.ipynb)  
Output:
 - Inline

