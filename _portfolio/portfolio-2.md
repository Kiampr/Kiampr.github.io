---
title: "Physics-Informed Neural Networks for CO₂ Storage"
excerpt: "PINNs embedding PDE conservation laws into training for accurate CO₂ plume simulation<br/><img src='/images/pinns-diagram.svg' style='max-width:100%; margin-top:0.5rem;'>"
collection: portfolio
---

<div style="text-align:center; margin: 1.5rem 0;">
  <img src="/images/co2-plume.svg" alt="CO2 plume migration in subsurface reservoir" style="max-width:100%; border-radius:8px; box-shadow: 0 2px 12px rgba(0,0,0,0.08);">
</div>

## Overview

Physics-informed neural networks (PINNs) offer a mesh-free approach to solving PDEs by embedding physical conservation laws directly into the training objective. This project developed a **sequential training strategy** for PINNs applied to CO₂ injection and storage simulation, dramatically improving convergence stability for problems with sharp saturation fronts.

<div style="text-align:center; margin: 1.5rem 0;">
  <img src="/images/pinns-diagram.svg" alt="PINN architecture diagram" style="max-width:100%; border-radius:8px; box-shadow: 0 2px 12px rgba(0,0,0,0.08);">
</div>

## Methods

- **Physics loss:** PDE residual of two-phase, two-component CO₂–brine transport equations added directly to the training objective
- **Sequential (curriculum) training:** domain expanded progressively in time, allowing the network to build accurate solutions incrementally without saturation-front divergence
- **Boundary and initial condition enforcement:** hard constraint approach ensuring exact satisfaction at boundaries
- **Benchmarking:** compared against classical finite-volume solver (DARTS) on heterogeneous reservoir test cases

## Why PINNs for CCUS?

CO₂ storage simulation involves sharp phase-change fronts and heterogeneous media that challenge both traditional solvers (convergence cost) and pure data-driven surrogates (generalisation). PINNs with physics constraints offer a middle ground: mesh-free, differentiable, and physically consistent even in data-sparse regimes.

## Publications

- [Mansour Pour, Voskov (2023) — Journal of Machine Learning for Modeling and Computing](https://www.dl.begellhouse.com/journals/558048804a15188a,24f8785e4156a0df,157258503daf8310.html)
