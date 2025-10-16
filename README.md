## Aman-Team — Waste Management Analysis (Iteration 1)

A simple, first-iteration analysis of municipal solid waste data across Indian cities. We clean and encode the dataset, scale features, cluster records, and prepare labels for a follow-up FLANN classifier. Plots compare model behavior under different expansion settings. This is Iteration 1; more iterations can be added if needed.

### What this project does
- Preprocesses `w.csv` (imputation if needed, label encoding, latitude/longitude split)
- Scales features: standardization → non-linear transform (log for positives) → min–max normalization
- Splits data (70/30)
- Clusters with K-Means into 3 groups (used as classes)
- Prepares train/test labels for a future FLANN model

### Key files
- `w.csv`: Waste dataset (cities, waste types, recycling rate, costs, landfill info, year)
- `new.ipynb`: Main notebook (same content is also under `Iteration 1/new.ipynb`)
- `Iteration 1/Results.pdf`: Consolidated results for this iteration
- Figures under `Iteration 1/`:
  - `Training Model comparision for 3 expansion.png`
  - `Training Model comparision for 5 expansion.png`
  - `Testing Model comparision for 3 expansion.png`
  - `Testing Model comparision for 5 expansion.png`

### How to run
1. Open `new.ipynb` (or `Iteration 1/new.ipynb`).
2. Run the first cell to install dependencies (pandas, numpy, tensorflow, matplotlib, seaborn, scikit-learn).
3. Ensure `w.csv` is in the project root.
4. Run cells top to bottom to reproduce preprocessing, clustering, and label preparation.

### Outputs you will see
- Console logs summarizing preprocessing steps and shapes
- K-Means cluster counts for train/test and centers
- Saved plots comparing training/testing performance for 3 vs 5 expansion settings in `Iteration 1/` (see the PNGs)
- Summary document: `Iteration 1/Results.pdf`

### Notes & next steps
- This is Iteration 1. Further iterations can be extended as required.

### Requirements
- Python with the packages auto-installed by the first notebook cell: `pandas`, `numpy`, `tensorflow`, `matplotlib`, `seaborn`, `scikit-learn`.