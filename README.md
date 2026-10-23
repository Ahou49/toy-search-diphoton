# Toy search for a new particle in the diphoton channel

M1 internship at LPCA (ATLAS group), 2025, supervised by Dr. Louie Corpe.
Search for a new particle decaying to two photons in simulated LHC data.
## Supervisors
Louie Corpe
## Goal
Build a complete analysis chain on simulated data: variable choice,
selection, fit, significance – following a blind analysis strategy.

## Method
- Selection of 6 discriminating variables among 14 kinematic observables
  (photon pT and isolation, jet multiplicity, missing energy, ...)
- Cut optimisation by maximising S/√B
- Fit of the diphoton invariant mass with a Gaussian (signal) plus an
  exponential (background)
- Significance: Z-score and p-value; cross-section limits via signal
  injection tests
- Random Forest classifier (scikit-learn) compared to the cut-based
  selection, with threshold optimisation on the F1 score
- Blind analysis: selection fixed before looking at the signal region

## Results
- Cut-based selection: 88% background rejection while keeping ~56% of
  the signal
- Dataset competition (data_2): 3.52σ excess, mass measured at
  625.7 ± 2.9 GeV, cross-section 0.11 ± 0.04 pb
- data_4 (background only): Z = 0.96σ, 95% CL upper limit σ < 0.08 pb
- Random Forest: retained events reduced from 12% to 4% compared to
  cuts, signal retention increased by 36%
## Tools
Python (numpy, pandas, matplotlib, scipy, scikit-learn).

## How to run
pip install -r requirements.txt
python scripts/run_selection.py
python scripts/fit_mass.py

## Data
Simulated samples provided by the ATLAS group at LPCA via internal CERN
storage. The data are not redistributed in this repository.
Contact ahlamalhadhur@gmail.com for more information about the samples.

## Repository structure
scripts/     analysis and fitting scripts
## Context
Code written during my M1 internship (2025) and published in 2026,
with the agreement of my internship supervisor.

## Contact
Ahlam Alhadhur – ahlamalhadhur@gmail.com
