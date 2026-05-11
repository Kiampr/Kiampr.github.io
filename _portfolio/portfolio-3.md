---
title: "Coupled Wellbore–Reservoir Digital Twin"
excerpt: "Digital twin combining wellbore flow dynamics with reservoir simulation for real-time geo-energy decisions<br/><img src='/images/wellbore-reservoir.svg' style='max-width:100%; margin-top:0.5rem;'>"
collection: portfolio
---

<div style="text-align:center; margin: 1.5rem 0;">
  <img src="/images/wellbore-reservoir.svg" alt="Coupled wellbore-reservoir model schematic" style="max-width:100%; border-radius:8px; box-shadow: 0 2px 12px rgba(0,0,0,0.08);">
</div>

## Overview

Accurate prediction of subsurface energy system behaviour requires tightly coupling **wellbore flow dynamics** (pressure, temperature, multiphase pipe flow) with **reservoir simulation** (multiphase flow in porous media, thermodynamics). This project developed a fully coupled digital twin framework using operator-based linearisation (OBL), enabling consistent and convergent solutions across the wellbore–reservoir interface.

## Methods

- **Operator-based linearisation (OBL):** both wellbore and reservoir equations expressed in a unified operator framework, enabling consistent Jacobian assembly and Newton iterations
- **Wellbore model:** drift-flux formulation for transient multiphase pipe flow with friction and heat exchange
- **Reservoir model:** compositional multiphase flow with CO₂ EOS and phase equilibrium calculations
- **Coupling:** iterative operator-splitting with convergence criteria at the wellbore–reservoir interface
- **Adaptive nonlinear solver:** trust-region modification for robust convergence at high injection rates

## Applications

- CO₂ injection well design and operational optimisation
- Geothermal doublet simulation and heat extraction monitoring
- Real-time wellbore–reservoir state estimation from surface measurements

## Publications

- [Mansour Pour, Voskov, Bruhn (2023) — Geoenergy Science and Technology (Coupled modelling)](https://www.sciencedirect.com/science/article/pii/S2949891023005134)
- [Mansour Pour, Voskov, Bruhn (2023) — Geoenergy Science and Technology (Nonlinear solver)](https://www.sciencedirect.com/science/article/pii/S2949891023002853)
