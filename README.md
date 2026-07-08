# CoDER-app

CoDER-app is an interactive visualization interface and reproducibility repository for the CoDER framework: Consistent Drug Efficacy Ranking.

## Data preprocessing and efficacy matrix generation

The CoDER algorithm operates on disease-specific drug efficacy matrices, where rows correspond to tissues and columns correspond to candidate drugs. In this repository, we provide the final efficacy matrices used in the experiments to ensure reproducibility of the CoDER ranking, baseline comparisons, and sensitivity analyses.

The upstream preprocessing pipeline used to construct the efficacy matrices from GTEx, TRRUST, DisGeNET, and DGIdb is maintained in a separate repository:

https://github.com/OmerKahveci03/Gene-Normalization-and-Mapping

That repository contains the scripts for gene normalization, mapping, and construction of disease-specific drug efficacy matrices. The present repository starts from the generated efficacy matrices and contains the CoDER implementation, experimental scripts, random seeds, parameter settings, baseline comparisons, and visualization code used in the manuscript.

To reproduce the results in the paper, users may either:
1. use the provided efficacy matrices directly, or
2. regenerate the matrices using the upstream preprocessing repository and then run the CoDER scripts in this repository.

## Repository Contents

- `efficacy.csv`: drug–tissue efficacy matrix (for Neurodegenerative diseases)used by the CoDER visualization.
- `CoDER_seed_exp.ipynb` – Reproducibility and seed-sensitivity experiments.
- `fullversion.ipynb`: notebook containing the main CoDER analysis pipeline.
- `index.html`: web-based visualization interface.
- `newnetwork05.html`: interactive drug-network visualization.
- `Datasets` : containing drug-gene association and disease-gene association datasets for neurodegenerative diseases, COPD (BPCO) and Diabetes.
- `Other algorithms`: contains Tissue-aware versions of Kemmeny, Schulze, and Ranked-Pair algorithms. 

## Reproducibility

To address stochasticity introduced by random partitioning, we evaluated CoDER using multiple random seeds.
To reproduce the results, replace the efficacy file name corresponding to the disease you want the results for.  

### Random Seeds

The seed sensitivity experiments were performed using:

```text
42, 43, 44, 45, 46, 47, 48, 49, 50, 51
