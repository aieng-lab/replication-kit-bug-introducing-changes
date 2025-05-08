# Replication Kit

This repository serves as the replication kit for the paper "An exploratory study of bug-introducing changes: what happens when bugs are introduced in open source software?".

## Content

- `complete_dataset` contains all relevant results as they appear in the paper, without intermediate steps.
- `data_analysis_replication/` contains the scripts used to generate tables for resolving disagreements and to analyze the fully coded variables.
  - Details about individual scripts can be found in the folder [README](/data_analysis_replication/README.md).
  - The results of the analysis can be found [here](/data_analysis_replication/output/)
- `data_collection_replication/` contains the scripts for sampling, as well as aggregating manually coded data from the rater spreadsheets and automatically collected data from SmartSHARK[^1].
  - Details about individual scripts can be found in the folder [README](/data_collection_replication/README.md).
  - The results of the sampling can be found [here](/data_collection_replication/sampling/output/)
  - The results of the data collection can be found [here](/data_collection_replication/labeling/output/)
- `smartshark_database` contains scripts to execute SmartSHARK[^1] for repository mining, as well as a pseudonymised MongoDB database dump and archives of the Nova and Elasticsearch repositories.

[^1]: https://smartshark.github.io
