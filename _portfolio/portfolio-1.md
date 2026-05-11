---
title: "Neural Operator Surrogates for Geophysical Simulation"
excerpt: "Fourier Neural Operators achieving ~10× speedup over classical PDE solvers for multiphase flow<br/><img src='/images/fno-speedup.svg' style='max-width:100%; margin-top:0.5rem;'>"
collection: portfolio
---

<div style="text-align:center; margin: 1.5rem 0;">
  <img src="/images/fno-speedup.svg" alt="FNO vs classical solver speedup" style="max-width:100%; border-radius:8px; box-shadow: 0 2px 12px rgba(0,0,0,0.08);">
</div>

## Overview

Classical PDE solvers for multiphase compositional flow are computationally expensive, limiting their use in real-time reservoir management and uncertainty quantification workflows. This project developed **Fourier Neural Operator (FNO) surrogates** trained on simulation data, achieving approximately **10× speedup** while preserving physical fidelity.

## Methods

- **Fourier Neural Operator (FNO):** a neural operator architecture that learns mappings between function spaces, well-suited to spatio-temporal PDE solutions on regular grids
- **Operator-based linearisation (OBL):** surrogate is trained in the operator space of the PDE rather than the solution space, yielding more compact and transferable representations
- **Multi-fidelity training:** coarse-grid simulations used to augment limited high-fidelity training data
- **Validation:** compared against full finite-volume reference solutions across heterogeneous reservoir configurations

## Applications

- Real-time CO₂ storage monitoring and history matching
- Uncertainty quantification for CCUS feasibility studies
- Rapid reservoir screening for geothermal siting

## Publications

- [Hadjisotiriou, Mansour Pour, Voskov (2023) — SPE RSC](https://doi.org/10.2118/212217-MS)
- [Mansour Pour, Voskov, Bruhn (2023) — Geoenergy Science and Technology](https://www.sciencedirect.com/science/article/pii/S2949891023002853)
