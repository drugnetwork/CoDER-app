# CoDER-app

CoDER-app is an interactive visualization interface and reproducibility repository for the CoDER framework: Consistent Drug Efficacy Ranking.

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
