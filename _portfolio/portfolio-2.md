---
title: "Nonlinear Solvers for Compositional Reservoir Simulation"
excerpt: "Trust-region globalization for robust convergence of compositional multiphase flow solvers<br/><img src='/images/nonlinear-convergence.svg' style='max-width:100%; margin-top:0.5rem;'>"
collection: portfolio
---

<div style="text-align:center; margin: 1.5rem 0;">
  <img src="/images/nonlinear-convergence.svg" alt="Compositional ternary diagram with trust-region solver trajectory" style="max-width:100%; border-radius:8px; box-shadow: 0 2px 12px rgba(0,0,0,0.08);">
</div>

## Overview

Compositional reservoir simulation involves coupled nonlinear PDEs whose solution traverses the **phase envelope** in composition space — the boundary between single-phase and two-phase coexistence shown in the ternary diagram above. Near this boundary, the residual function becomes highly non-smooth, and **standard Newton-Raphson iterations frequently fail** to converge: step sizes become erratic, the iterate jumps in and out of the two-phase region, and progress stalls.

## Approach

This project developed a **trust-region globalization strategy** for nonlinear solvers within the operator-based linearisation (OBL) framework. Rather than taking the full Newton step at every iteration, the method adapts the step length based on a quadratic model of the residual reduction, keeping the iterate within a region of trust where the linearisation is reliable. As a result, the solver remains feasible across the phase envelope and converges robustly even on cases that defeat standard Newton.

The same framework was extended to **discrete fracture network (DFN) models**, where extreme heterogeneity and high nonlinear contrast make convergence even harder. An adaptive variant combining trust-region with operator-based linearisation handles these cases without manual tuning of step-size parameters.

## Key results

- Robust convergence on CO₂ injection cases in saline aquifers and depleted reservoirs
- Reduced nonlinear iteration counts compared to standard Newton in challenging convergence regimes
- Adaptive variant successful on discrete fracture network problems with high permeability contrast
- Framework integrated into the DARTS open-source reservoir simulation framework

## Publications

- [Mansour Pour, Voskov, Bruhn (2023). Nonlinear solver based on trust region approximation for CO₂ utilization and storage in subsurface reservoir. *Geoenergy Science and Technology*.](https://www.sciencedirect.com/science/article/pii/S2949891023002853)
- [Mansour Pour, Voskov (2020). Adaptive nonlinear solver for a discrete fracture model in operator-based linearization framework. *17th ECMOR*.](https://doi.org/10.3997/2214-4609.202035094)
