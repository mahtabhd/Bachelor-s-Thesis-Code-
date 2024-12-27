# Protein Dynamics Analysis: Semi-Rigid Domain Detection Algorithm

This repository contains the implementation of the algorithm developed for identifying semi-rigid domains and super-domains in proteins, as described in my bachelor's thesis: **"Hierarchical Algorithm for Identifying Semi-Rigid Domains in Proteins"**.

## Overview

Understanding protein dynamics is crucial for unraveling biological functions. This algorithm processes molecular dynamics (MD) simulation data to partition proteins into semi-rigid domains and larger super-domains. It combines:
- **Greedy approach** for domain construction
- **Divide-and-conquer strategy** for super-domain identification
- **Data-driven parameter determination** using Gaussian Mixture Models (GMMs)

The method has been tested on three proteins of increasing complexity:
1. **Glycophorin A**
2. **β2-Adrenergic Receptor**
3. **Viral Capsid Protein**

For more details, refer to my [thesis document](https://aaltodoc.aalto.fi).

---

## Features

- **Domain Construction:** Identifies rigid clusters of residues based on distance deviation matrices.
- **Super-Domain Construction:** Groups domains into larger rigid regions using Union-Find and threshold filtering.
- **Data-Driven Parameter Search:** Utilizes GMMs to determine biologically meaningful thresholds.
- **Visualization:** Outputs results compatible with molecular visualization tools (e.g., VMD, PyMOL).

---

## Repository Structure

- `/src`: Source code for the algorithm
  - `hierarchical_superdomains.ipynb`: Implements the algorithm
- `/data`: Example input MD trajectory and coordinate files (from viral capsid protein test case)
- `README.md`: Repository documentation

---

## Requirements

- MDAnalysis
- Scikit-learn
- NumPy
- Matplotlib


## Author Notes:
Please cite my thesis and this git repository (developed under supervision of the Biological Physics and Soft Matter group of University of Helsinki) if you used the algorithm.
