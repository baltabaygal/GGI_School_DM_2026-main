# GGI School DM 2026 Exercises

This repository contains Python and Mathematica material for the GGI 2026 dark-matter indirect-detection exercises.

## Contents

- `GGI_2026_DM_exercises.pdf`: exercise sheet (main reference).
- `Jfact.ipynb`: density profiles, line-of-sight integrals, J-factor (and D-style) calculations.
- `Ngamma.ipynb`: prompt gamma-yield calculations using tabulated spectra.
- `Power.ipynb`: secondary-emission ingredients (IC, synchrotron, bremsstrahlung, gas/photon/magnetic models).
- `CosmiXs.py`: helper to interpolate annihilation spectra from tabulated files.
- `CosmiXs/AtProduction-Gamma.dat`, `CosmiXs/AtProduction-Positrons.dat`: spectra tables used by `CosmiXs.py`.
- `PPPC4DMID.m.zip`, `*.nb`: Mathematica versions/assets.

## Environment

Python dependencies:

- `numpy`
- `scipy`
- `pandas`
- `matplotlib`
- `jupyter`

If you use conda (example):

```bash
conda create -n ggi_dm python=3.11 numpy scipy pandas matplotlib jupyter -y
conda activate ggi_dm
```

## Run

From the repository root:

```bash
jupyter notebook
```

Open notebooks in this order:

1. `Jfact.ipynb`
2. `Ngamma.ipynb`
3. `Power.ipynb`

## Notes

- `Ngamma.ipynb` calls:
  - `annihilation_spectrum(..., path='CosmiXs')`
  so the local spectra tables are used directly.
- Units are mostly natural units (GeV-based), following the exercise sheet.
- Numerical integrations may show warnings near cusps; this is common for steep profiles and tight tolerances.

## Current Progress (in-notebook added sections)

The notebooks include added labeled cells for:

- `Jfact.ipynb`: `Question 1.1.1`, `1.1.2`, `1.1.3`, `2.1`
- `Ngamma.ipynb`: `Question 1.2.1`, `1.3.1`
- `Power.ipynb`: `Question 3.1.1`, `3.1.2`

These are organized as markdown prompt + solution code cells for direct execution.
