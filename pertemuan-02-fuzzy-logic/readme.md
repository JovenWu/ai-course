# Week 2 — Fuzzy Logic

## Overview

This assignment implements fuzzy logic examples for two cases:

- Netflix movie-quality scoring: see the notebook [netflix-recomendation.ipynb](netflix-recomendation.ipynb) and the helper symbol `compute_movie_quality` inside that notebook.
- Washing machine controller: primary focus of this report — see [washing-machine-fuzzy.ipynb](washing-machine-fuzzy.ipynb).

## Washing Machine Case — Summary

Goal: design a fuzzy controller that maps:

- LoadWeight (kg), DirtLevel (1–5), and FabricType (1 = Normal, 2 = Delicate)
  to outputs:
- WashTime (minutes), WaterLevel (Low/Medium/High), SpinSpeed (Slow/Medium/Fast).

Key functions (inside the notebook):

- `simulate_wash` — runs inference for a single sample (in washing-machine-fuzzy.ipynb).
- `process_csv` — batch processes a CSV input and writes outputs (in washing-machine-fuzzy.ipynb).

The implemented pipeline:

1. Read inputs from washing-data.csv.
2. For each row, run the fuzzy controller (`simulate_wash`) to compute numeric WashTime and derive categorical WaterLevel and SpinSpeed.
3. Append results and save to washing_output.csv.

## Files in this folder

- netflix-recomendation.ipynb — fuzzy scoring for movies.
- washing-machine-fuzzy.ipynb — washing machine fuzzy controller (contains `simulate_wash` and `process_csv`).
- washing-data.csv — example inputs.
- washing_output.csv — example outputs produced by the notebook.
- data.csv — dataset used for the Netflix notebook.
- top-movies.csv — exported top movies from the Netflix notebook.
- requirements.txt — environment dependencies.
- readme.md — this file.

## How to run the washing-machine example (local)

1. Open washing-machine-fuzzy.ipynb in Jupyter or VS Code.
2. Ensure Python environment contains packages from requirements.txt.
3. Run all notebook cells. Or run the batch helper inside the notebook:
   - The notebook entrypoint calls `process_csv` which reads washing-data.csv and writes washing_output.csv.
4. Inspect outputs in washing_output.csv.

## Fuzzy design notes (brief)

- Inputs use overlapping membership functions to handle uncertainty.
- Rules are a compact set mapping common situations (e.g., Heavy + High dirt => Long wash, High water, Fast spin).
- Defuzzification yields numeric WashTime; categorical WaterLevel/SpinSpeed are derived using membership strengths and thresholds.

## Where to look in the code

- Fuzzy sets, rules, and controller creation: see washing-machine-fuzzy.ipynb.
- Per-row inference: `simulate_wash` in washing-machine-fuzzy.ipynb.
- CSV batch processing and example run: `process_csv` in washing-machine-fuzzy.ipynb.

## Notes

- The Netflix example uses a separate fuzzy model; see netflix-recomendation.ipynb and its CSV outputs (top-movies.csv).
- For reproducibility, install dependencies from requirements.txt.
