# Getting Started

Overall prerequisites:
> 1. Create or copy [all_information](/input/all_information.csv) to the repository
> 2. Create or copy [variable_overview](/input/variables_overview.csv) to the repository
> 3. Complete [.env.sample](.env.sample) and rename it to `.env`


## Sampling

Scripts for sampling can be found in folder `/sampling`.

Prerequisites for sampling:
> 1. Create .csv files [nova_bic.csv](/sampling/nova_bic.csv) and [elasticsearch_bic.csv](/sampling/elasticsearch_bic.csv)
> 2. Add columns ``bug`` and ``bic_revision_hash`` according to bug-introducing dataset.

To run the sampling for nova and elastic search, execute the scripts [nova_sampling](/sampling/nova_sampling.ipynb) and [elasticsearch_sampling](/sampling/elasticsearch_sampling.ipynb).

## Automatic Variables

Scripts for obtaining the automatic variables can be found in folder `/labeling/automatic_labeling`.

Prerequisites to obtaining the automatic variables:
> 1. Run Smartshark
> 2. Run [pr_helper](/labeling/automatic_labeling/pr_helper/elasticsearch_get_reviews_from_pr_html.ipynb)

After running [get_automatic_variables](/labeling/automatic_labeling/get_automatic_variables.ipynb), .csv files will be stored in `/labeling/automatic_labeling/output`.

## Manual Variables

Scripts for processing the manual variables can be found in folder `/labeling/manual_variables`.

Prerequisites to obtaining the manual variables:
> 1. Complete manual labeling
> 2. Store manual labeling results and merged_codebook excel in files `/labeling/manual_labeling/input/rater_files`

After running [process_manual_variables](/labeling/manual_labeling/process_manual_labels.ipynb), files for resolving conflicts are stored in folder `/labeling/manual_labeling/output/diagreements`. Once conflicts were manually resolved, those files should be stored in `/labeling/manual_labeling/input/disagreements_resolved`.

The script [interrater_agreement](/labeling/manual_labeling/interrater_agreement.ipynb) can be used to calculate the interrater agreement.

## Joining manual and automatic datasets

The script for joining the datasets into a final Excel sheet is [joining_datasets](/labeling/joining_datasets.ipynb). The output is stored in folder `/labeling/output/coded_dataset`.