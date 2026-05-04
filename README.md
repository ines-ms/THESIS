# Thesis Model — AI Inference Infrastructure Simulation

Python simulation code for the BIE Final Project thesis
**"AI Inference Infrastructure Under Uncertainty: A Simulation-Based Real Options Analysis of Sizing and Revision"**

IE University, BIE Final Project, May 2026.

Author: Inés Marí Sanguino. Supervisor: Iñigo Cavestany.

## Overview

The simulation evaluates infrastructure commitment strategies for a mid-size enterprise running AI inference workloads, comparing cloud-only deployment against hybrid configurations under demand uncertainty and declining cloud prices. The model implements:

- A geometric Brownian motion demand process with Poisson jumps
- Four cost-computation regimes: no revision, re-estimation forecast, sub-simulation, and perfect foresight
- A jump-aware maximum likelihood estimator used at the t=12 revision point
- Sensitivity sweeps across overhead, salvage, cloud price, demand parameters, and cloud price decline rate

## Requirements

- Python 3.11+
- numpy, pandas, scipy, matplotlib

Install dependencies:

\`\`\`
pip install numpy pandas scipy matplotlib
\`\`\`

## Running the simulation

\`\`\`
python thesis_model.py
\`\`\`

The script generates all tables and figures referenced in Chapter 5 and the appendix.

Random seed: `RANDOM_SEED = 42` (fixed for reproducibility).

Approximate runtime: 15 minutes on a standard laptop.

## Outputs

Running the script produces:

- Strategy comparison results (Appendix A)
- Parameter estimation quality at t=12 (Appendix B)
- Sensitivity tables: overhead, salvage, cloud starting price (Appendix C)
- Cloud price decline sweep (Appendix D)
- Break-even sweep (Appendix E)
- Combined heatmap of option value across volatility and cloud decline (Appendix F)

## Acknowledgements

This simulation was developed by Inés Marí Sanguino as part of the BIE Final Project at IE University. Generative AI tools (Claude, Anthropic) were used for code review, debugging, and methodological consultation during development. The author takes full responsibility for the implementation, results, and interpretations.
