# Cell Dynamics Roadmap

Theme: the collective dynamics and shape of the cells forming the lumenoid, from 2D CCW
rotation in the planar colony to vortices and spirals on the 3D lumenoid surface, modeled
as one chiral active polar/nematic gel across geometries.

## Phase I — Formulation and Solver

### Active Polar Gel on S²

* Surface operators (grad, div, curl, scalar/vector Laplacian) on a Gauss–Legendre × Fourier grid
* Toroidal-VSH Stokes inversion (screened/Brinkman)
* Polarity dynamics: flow alignment, vorticity, Frank elasticity, chirality

### Numerical Hardening

* Correct the scalar-Laplacian sign error (anti-diffusive Frank force) and the γ₁ factor
* Move to IMEX time-stepping (explicit RK4 + implicit Frank damping)
* Validation suite (eigenmodes, superposition, Kruse sin-law, aster/vortex, stability)

### Active Driving Mechanism

* Reformulate the body force as a selectable traction / active-stress model
* Default: monopolar traction **f** = γv₀**p** (self-propulsion speed v₀ scaling with polarity; no surface derivatives of **p** required)
* Legacy: dipolar active stress divergence −∇_S(ζ**p**⊗**p**) retained for comparison
* Physical basis: traction dominates in substrate-bound confluent epithelia (Pricoupenko et al. 2024; Blanch-Mercader & Casademunt 2017)

Status: Complete

---

## Phase II — Why Spirals Need a Source

### Theory

* Show incompressible toroidal flow yields only closed vortex streamlines
* Show a pure aster (point-source texture) drives zero flow

### Compressible Extension

* Surface mass balance with an out-of-plane source: div_S v = s
* Spheroidal velocity v = ∇_S Φ, Δ_S Φ = s
* Validate the point-source Green's function v_θ = cot(θ/2)/(4πR)
* Implement a generic stochastic source (zero-mean, band-limited, OU-in-time)

Status: Complete

---

## Phase III — Confront 3D Experiments (lattice light-sheet)

### Existing data

* Two lattice light-sheet nuclear-trajectory datasets; surface streamlines computed (velocity-magnitude background) showing vortices/spiral cores.
* Project nuclear velocity onto the shell; extract streamlines, vorticity, and surface divergence; locate spiral cores and defects.

### Planned: 3 × 48-hour runs (>1 cell division)

* (i) nuclear growth in volume vs time
* (ii) cell count vs time
* (iii) variation of streamlines with time — i.e. with lumenoid size R (which enters the model directly)
* (iv) correlation of radial (r-direction) nuclear motion and mitosis with the streamlines — direct test of the out-of-plane / INM source

Status: In Progress (2 datasets analyzed; 3 longer runs planned)

---

## Phase IV — Mechanism Identification and Perturbations

### Calibration

* Fit source spatial pattern, amplitude, and time correlation to data
* Co-estimate traction amplitude γv₀, active and chiral parameters; test the size-R scaling
* Compare traction-dominant vs active-stress-dominant fits to constrain which regime applies

### Perturbation experiments (repeat lattice light-sheet)

* **Rapamycin** (reduced growth): isolate growth rate → growth-generated active stress → magnitude and form of collective motion (and, via fewer divisions, the INM source / spirals).
* **TJP1 (ZO-1) knockdown:** coupled change to shell mechanics and ion permeability; tunable knockdown fraction enables **mosaic / mixed-population** experiments probing how locally perturbed cells reorganize the global collective motion.

Status: Planned

---

## Phase V — 2D Planar Rotation (flat limit of the same model)

### Theory

* Take the flat-geometry limit of the chiral active-gel model
* Predict chiral CCW collective rotation from the chiral active stress
* Check that one parameter set links 2D rotation sense and 3D spiral handedness

### Data (label-free nuclear tracking, ZSD-20× air objective)

* Repeat the robust CCW-rotation observation during 2D colony formation
* Measure angular velocity vs distance from the colony edge, across colony sizes (edge/screening-length and size-scaling test)
* Track the onset/clearing of rotation through the 2D→3D transition

Status: Robust preliminary observation in hand; quantitative/size-resolved measurement planned

---

## Phase VI — Coupling to Cell Shape

* Couple the collective flow to the flat→columnar/pseudostratified shape change
* Couple to the 2D→3D geometric transition (layer closure into a sphere)
* Test whether shape perturbations change the flow regime, and vice versa

Status: Planned

---

## Phase VII — Synthesis

### Scientific Story

Question:
What governs the collective dynamics and shape of the cells forming the lumenoid — the 2D CCW rotation and the 3D vortices/spirals?

Mechanism:
A chiral active polar/nematic cell layer drives flow primarily through cell–substrate traction (monopolar body force proportional to polarity **p**) rather than active stress gradients. On the flat geometry this generates CCW collective rotation; on the closed sphere, the Poincaré–Hopf constraint forces +1 defects and the traction-driven toroidal flow produces vortices; cell-cycle-gated out-of-plane nuclear motion (INM) adds a compressible (spheroidal) component that turns vortices into spirals. Cell shape co-evolves with the flow.

Validation:
2D rotation statistics, surface-divergence measurements at 3D spiral cores, and chirality / cell-cycle / INM perturbations — all within one parameter framework.

### Remaining Tasks

* Quantitative phase diagram (rotation / aster / vortex / spiral) vs activity, chirality, source strength, and geometry
* Uncertainty and identifiability analysis
* Manuscript figures and narrative

Target Outcome:

A predictive framework connecting chirality, activity, topological defects, cell-cycle-gated nuclear motion, and geometry to the collective dynamics and shape of cells across lumenoid morphogenesis.
