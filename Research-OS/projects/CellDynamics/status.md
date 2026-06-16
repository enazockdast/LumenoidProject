# Project Status

Last Updated: 2026-06-14

## Current Stage

Framing the project around the collective dynamics and shape of the cells forming the lumenoid (2D CCW rotation → 3D vortices/spirals). The 3D surface-flow model is built and validated; the 2D rotation limit and the coupling to cell shape are still to be developed.

## Completed

Data & tools:

* Robust preliminary observation of CCW collective cell motion during 2D colony formation.
* Label-free model for the ZSD-20× air objective: tracks nuclei from brightfield (enables long-term 2D tracking).
* Two lattice light-sheet datasets of nuclear trajectories on lumenoids; surface streamlines computed (velocity-magnitude background) showing vortices/spiral cores.

Modeling & numerics:

* Audit of the active-polar-gel formulation and code (surface operators, Stokes solver, polarity dynamics, tests).
* Fixed a critical scalar-Laplacian sign error that had made the Frank elastic force anti-diffusive; corrected a stray 1/γ₁ factor in the polarity equation.
* Replaced the unstable explicit time-stepping with an IMEX scheme (explicit RK4 + implicit spectral Frank damping), enabling a ~5× larger timestep.
* Hardened the validation suite (sign fix, IMEX, stability check, point-source Green's function); 9/9 tests pass.
* Showed analytically and numerically that the incompressible toroidal flow gives only closed vortex loops (no point-source spirals), and that a pure aster drives zero flow.
* Derived and implemented the compressible source extension (continuity div_S v = s; spheroidal flow v = ∇_S Φ); validated the point-source Green's function v_θ = cot(θ/2)/(4πR) to <10⁻³.
* Implemented a generic stochastic source (zero-mean, band-limited, Ornstein–Uhlenbeck-in-time) in MATLAB and Python; documented in the formulation notes.
* Reformulated the active body force as a **traction / self-propulsion term**: each cell crawls along its polarity with speed v₀, giving a monopolar body force **f** = γv₀**p**. This replaces the active-stress divergence −∇_S(ζ**p**⊗**p**) as the default driving mechanism. Physical motivation: traction-force and stress microscopy in confluent epithelia (Pricoupenko et al. 2024; Blanch-Mercader & Casademunt 2017) show the monopolar traction term dominates the dipolar active stress. The key mechanistic distinction: the monopolar force drives flow from a spatially uniform polarity field (including the full-aster state), whereas the dipolar term vanishes for uniform **p**. The force model is now selectable (`'traction'` default, `'stress'` legacy, `'both'`).

## In Progress

* Extracting collective-motion metrics from data: 2D colony rotation (CCW bias, angular velocity, vorticity) and, in 3D, streamline topology and surface divergence of the projected nuclear velocity field.
* Specifying the out-of-plane source model from data (spatial pattern, amplitude, temporal correlation).

## Upcoming Milestones

1. **Repeat 2D CCW observation** and, using label-free brightfield tracking, measure angular velocity vs distance from the colony edge across colony sizes; compare to the active-nematic prediction and its size scaling.
2. **3 × 48-hour lattice light-sheet runs** (>1 division) to measure: (i) nuclear volume vs time, (ii) cell count vs time, (iii) streamlines vs time/size R, (iv) radial nuclear motion & mitosis vs streamlines (source test).
3. Reproduce 2D rotation and 3D vortices/spirals from the flat- and spherical-geometry limits of one chiral active-gel parameter set; test size-R scaling.
4. **Rapamycin** runs: growth rate → growth-generated active stress → magnitude/form of collective motion.
5. **TJP1 (ZO-1)** runs, including **mosaic** (tunable % knockdown): disentangle mechanics vs permeability and probe how locally perturbed cells reshape global collective motion.
6. Couple the collective flow to cell shape and the 2D→3D transition.

## Scientific Risks

* The 2D rotation and 3D spirals may not share a single parameter set (the unifying hypothesis could fail).
* Spirals could arise from in-plane effects (projection artifacts, chirality) rather than out-of-plane flux.
* The source model is under-determined without cell-cycle / INM data.
* The kinematic (continuity-only) source flow neglects viscous coupling of the radial flux; a full compressible-Stokes treatment may be needed.

## Opportunities

* One chiral active-gel framework spanning the 2D→3D morphogenesis trajectory (rotation → vortices/spirals).
* Connects cell-cycle biology (INM) to active-matter hydrodynamics on curved surfaces.
* Yields a quantitative defect/flow phase diagram (aster / vortex / spiral) for curved active gels.
* Links collective dynamics to cell shape — a candidate "knob" for movement and shape control.
* Shared numerical framework (pseudospectral S² solver) reusable across CellDynamics and related projects.
