---
title: "Neural Operators and Physics-Informed Neural Networks for Geophysical Simulation"
excerpt: "Combining Fourier Neural Operators and PINNs to accelerate and constrain compositional flow simulation<br/><img src='/images/pinns-diagram.svg' style='max-width:100%; margin-top:0.5rem;'>"
collection: portfolio
---

<div style="text-align:center; margin: 1.5rem 0;">
  <img src="/images/pinns-diagram.svg" alt="Physics-informed neural network architecture" style="max-width:100%; border-radius:8px; box-shadow: 0 2px 12px rgba(0,0,0,0.08);">
</div>

## Overview

Classical PDE solvers for multiphase compositional flow are computationally expensive, limiting their use in real-time reservoir management and uncertainty quantification. At the same time, pure data-driven surrogates often struggle with physical fidelity in data-sparse regimes. This work combines two complementary deep-learning approaches — **Fourier Neural Operators (FNO)** for fast simulation and **Physics-Informed Neural Networks (PINNs)** for embedded physical consistency — to address both speed and accuracy.

## Fourier Neural Operators (FNO)

FNOs learn mappings between function spaces, well-suited to spatio-temporal PDE solutions on regular grids. Trained on simulation data from a classical PDE solver, the FNO surrogate achieves approximately **10× speedup** while preserving physical accuracy across heterogeneous reservoir configurations. The operator is trained in the operator space of the PDE (operator-based linearisation, OBL), yielding compact and transferable representations.

## Physics-Informed Neural Networks (PINNs)

PINNs offer a mesh-free approach to PDE solution by embedding conservation laws directly into the training loss. A **sequential (curriculum) training strategy** progressively expands the spatio-temporal training domain, dramatically improving convergence stability for problems with sharp saturation fronts. This makes PINNs viable for CO₂ injection scenarios in heterogeneous media that are challenging for both classical solvers and standard data-driven approaches.

## Why combine them?

| Method | Strength | Limitation |
|---|---|---|
| Classical PDE solver | Physically rigorous | Slow, expensive |
| FNO surrogate | Fast, generalises across configurations | Requires simulation data; needs validation |
| PINN | Mesh-free; physics constraints built-in | Training stability with sharp fronts |

Used together, FNO surrogates provide fast inference for scenarios with available training data, while PINNs handle physically informed prediction in data-sparse regimes. The shared theme — **embedding or learning physical structure inside the neural architecture** — is the basis for interpretable, trustworthy scientific ML.

## Publications

- [Hadjisotiriou, Mansour Pour, Voskov (2023). Application of deep neural networks to the operator space of nonlinear PDE for physics-based proxy modelling. *SPE Reservoir Simulation Conference*.](https://doi.org/10.2118/212217-MS)
- [Mansour Pour, Voskov (2023). Physics-informed neural networks based on sequential training for CO₂ utilization and storage in subsurface reservoir. *Journal of Machine Learning for Modeling and Computing*.](https://www.dl.begellhouse.com/journals/558048804a15188a,24f8785e4156a0df,157258503daf8310.html)
