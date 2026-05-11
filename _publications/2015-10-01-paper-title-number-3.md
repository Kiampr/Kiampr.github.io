---
title: "Physics-informed neural networks based on sequential training for CO₂ utilization and storage in subsurface reservoir"
collection: publications
category: manuscripts
permalink: /publications/2023-pinns-co2/
excerpt: 'Sequential training strategy for PINNs applied to compositional CO₂ storage simulation, embedding PDE conservation laws into the training loss for physics-consistent predictions.'
date: 2023-04-01
venue: 'Journal of Machine Learning for Modeling and Computing'
paperurl: 'https://www.dl.begellhouse.com/journals/558048804a15188a,24f8785e4156a0df,157258503daf8310.html'
citation: 'K. Mansour Pour, D.V. Voskov (2023). "Physics-informed neural networks based on sequential training for CO₂ utilization and storage in subsurface reservoir." <i>Journal of Machine Learning for Modeling and Computing</i>.'
---

This work develops a **sequential (curriculum) training strategy** for physics-informed neural networks that progressively expands the spatio-temporal training domain, dramatically improving convergence stability and accuracy for CO₂ injection scenarios with sharp saturation fronts.

**Key contributions:**
- Sequential training strategy for PINNs in compositional transport problems
- Physics loss formulation for two-phase, two-component CO₂–brine system
- Convergence to physically accurate solutions for challenging heterogeneous reservoirs
- Benchmarked against classical finite-volume solver reference solutions

<div style="text-align:center; margin: 1.5rem 0;">
  <img src="/images/pinns-diagram.svg" alt="PINN architecture for CO2 storage simulation" style="max-width:100%; border-radius:8px;">
</div>

[Read paper →](https://www.dl.begellhouse.com/journals/558048804a15188a,24f8785e4156a0df,157258503daf8310.html)
