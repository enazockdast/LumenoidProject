# Cell Dynamics

## Scientific Question

What governs the **collective dynamics and shape of the cells that form the lumenoid** — from the chiral, counter-clockwise (CCW) collective rotation of cells in the 2D planar colony, through the 2D→3D transition, to the vortices and spirals seen in the cell/nuclear flow fields on the 3D lumenoid surface?

This is the "Understanding to Build" goal of the CellScapes program applied to cell dynamics: *identify the cellular mechanisms that form and maintain tissue-scale collective motion and shape*.

## Motivation

Lumenoid morphogenesis begins as a quasi-2D hiPSC colony and proceeds to a hollow 3D spherical shell. Across this trajectory the cell layer shows striking, organized collective motion:

* In the **2D planar tissue** (before the 3D transition), cells undergo coordinated **chiral CCW rotation**.
* On the **3D lumenoid surface**, the projected cell/nuclear velocity fields organize into **vortices and spirals** (the spirals having point-source/sink cores).

These are two expressions of one theme — the collective dynamics and shape of the cell layer — and plausibly of one underlying physics: a **chiral active polar/nematic cell layer** whose behavior depends on geometry (flat plane vs closed sphere), topology, and out-of-plane cell motion. The cell-shape change that accompanies the transition (flat → columnar/pseudostratified) is part of the same story. Understanding this is necessary to explain how the tissue forms and maintains its architecture and, ultimately, to make movement and shape controllable "knobs."

## Central Hypothesis

The cell layer behaves as a **chiral active polar/nematic gel**. The same active and chiral stresses that drive coordinated CCW rotation in the flat colony drive vortices and spirals once the layer closes into a sphere, where the Poincaré–Hopf constraint forces +1 defects.

* Purely **in-plane (incompressible)** active/chiral flow accounts for rotation and vortices (closed streamlines).
* The **spirals with point sources** additionally require **out-of-plane (radial) nuclear motion** — interkinetic nuclear migration (INM) — which, projected onto the surface, acts as a mass source/sink that turns vortices into spirals.

Cell shape (e.g. columnar/pseudostratified thickening) and the 2D→3D geometric transition are coupled to these flows.

## Approach

**2D planar colonies (label-free nuclear tracking).** A trained label-free model for the ZSD-20× air objective recovers nuclei from brightfield, enabling long-term tracking without fluorescence. Plan:

* Repeat the (robust, preliminary) CCW-rotation observation during 2D colony formation.
* Track nuclei and measure the **angular velocity as a function of distance from the colony edge**, for **colonies of different size** — a direct test of the active-nematic prediction (edge/screening-length-controlled rotation profile and its size scaling).

**3D lumenoids (lattice light-sheet nuclear trajectories).** Two datasets exist; surface streamlines have been computed (velocity-magnitude background) and show vortices/spiral cores. Plan: **3 additional 48-hour lattice light-sheet experiments** (long enough for >1 cell division) to measure:

1. nuclear growth in volume vs time;
2. cell count vs time;
3. variation of streamlines with time — equivalently with **lumenoid size R, which enters the model directly**;
4. correlation of **radial (r-direction) nuclear motion and mitosis with the streamlines** (test of the out-of-plane / INM source).

**Perturbations (repeat the lattice light-sheet experiments).**

* **Rapamycin** (reduced growth): isolate the effect of growth rate — and the active stress it generates — on the magnitude and form of collective motion.
* **TJP1 (ZO-1) knockdown:** affects both shell mechanics and ion permeability, so it may act in non-trivial, coupled ways. Because it is a genetic (iCRISPRi) knockdown, the **fraction of expressing cells is tunable → mosaic / mixed-population** experiments probing how locally perturbed cells reorganize the global collective motion.

### Modeling

Chiral active polar/nematic gel hydrodynamics, in two geometries:

* **Flat (2D colony):** predict chiral CCW collective rotation from the chiral active stress.
* **Sphere (3D lumenoid):** coupled surface Stokes + polarity dynamics (Kruse et al. with a chiral extension), pseudospectral solver, IMEX time-stepping; the toroidal (vortex) flow plus a stochastic out-of-plane mass source (INM) giving the spheroidal/spiral component.
* Couple the flow to **shape**: the 2D→3D transition and the columnar shape change.

**Active driving mechanism.** The model supports two physically distinct ways the polarity field p drives flow:

* **Self-propulsion / traction (monopolar, default):** each cell crawls along its polarity direction with speed v₀; the cell–substrate friction reaction gives a body force **f** = γv₀**p** proportional to **p** itself. This force is nonzero even for uniform **p** and requires no surface derivatives. For substrate-bound confluent epithelia, traction-force and stress microscopy show this term dominates (Pricoupenko et al. 2024; Blanch-Mercader & Casademunt 2017).
* **Active stress divergence (dipolar, legacy):** **f** = −∇_S(ζ**p**⊗**p**); vanishes for uniform **p**, is large near defects and polarity gradients, and requires surface derivatives of **p**.

The traction model is the default (`force_model = 'traction'`, parameter `γv₀`); the active-stress model is retained for comparison (`force_model = 'stress'`). Both can be combined (`force_model = 'both'`).

## Key Results

Preliminary experimental observations:

* CCW collective cell motion during 2D colony formation is a **robust** preliminary observation (to be repeated).
* Surface streamlines computed from a lattice light-sheet lumenoid dataset show **vortices and spiral cores over a spatially heterogeneous speed field** — consistent with the active-nematic + out-of-plane-source picture.

So far the modeling effort has focused on the 3D surface-flow regime:

* Audited and corrected the active-gel formulation/solver (surface-Laplacian sign error; moved to a stable, ~5× faster IMEX scheme); validation suite passes (9/9).
* Established that the incompressible (toroidal) active flow produces only closed vortex loops about the defects — a pure aster drives zero flow — so spirals with point sources cannot come from the in-surface stress alone.
* Implemented and validated the out-of-plane source (INM model): the point-source velocity Green's function v_θ = cot(θ/2)/(4πR) is reproduced to <10⁻³, and the coupled solver produces stable, spiral-capable flow.
* Reformulated the active body force as a **traction/self-propulsion term** f = γv₀**p** (monopolar). This is motivated by experimental evidence that substrate traction dominates active stress in substrate-bound confluent epithelia, and by the physical distinction that the monopolar force drives flow even from a spatially uniform polarity field, whereas the dipolar stress divergence requires polarity gradients.

The 2D CCW-rotation limit of the same framework, and its coupling to cell shape, are the next steps.

## Long-Term Goal

A unified, predictive model of **collective cell dynamics and shape across lumenoid morphogenesis** — linking chirality, activity, topological defects, cell-cycle-gated nuclear motion, and geometry — that explains 2D CCW rotation and 3D vortices/spirals within one framework and connects them to tissue shape and movement.

## Foundational References

`★` = review / synthesis.

- Kruse, K., Joanny, J.-F., Jülicher, F., Prost, J. & Sekimoto, K. *Asters, Vortices, and Rotating Spirals in Active Gels of Polar Filaments.* Physical Review Letters 92, 078101 (2004). — `Asters_Vortices_and_Rotating_Spirals_in.pdf` — the active-gel model basis for this project.
- ★ Doostmohammadi, A., Ignés-Mullol, J., Yeomans, J. M. & Sagués, F. *Active nematics.* Nature Communications 9, 3246 (2018). — `ActiveNematics_Review.pdf`
- ★ Brückner, D. B. & Broedersz, C. P. *Learning dynamical models of single and collective cell migration: a review.* Reports on Progress in Physics 87, 056601 (2024). — `Review_LearningCellInteractions_Broedersz.pdf`
- Duclos, G., Erlenkämper, C., Joanny, J.-F. & Silberzan, P. *Topological defects in confined populations of spindle-shaped cells.* Nature Physics 13, 58–62 (2017). — `DefectDonfinedSpaceSpirals.pdf`
- ★ Gómez-González, M., Latorre, E., Arroyo, M. & Trepat, X. *Measuring mechanical stress in living tissues.* Nature Reviews Physics 2, 300–317 (2020). — `Good recent review.pdf`
- Pricoupenko, N., Marsigliesi, F., Marcq, P., Blanch-Mercader, C. & Bonnet, I. *Src kinase slows collective rotation of confined epithelial cell monolayers.* Soft Matter 20, 9273–9285 (2024). doi:10.1039/d4sm00827h — traction-force microscopy showing traction dominates active stress in confluent epithelia.
- Blanch-Mercader, C. & Casademunt, J. *Hydrodynamic instabilities, waves and turbulence in spreading epithelia.* Soft Matter 13, 6913–6928 (2017). doi:10.1039/c7sm01128h — traction-controlled tissue-scale kinematics in spreading monolayers.

Full corpus: `Literature/` (see `Literature/outputs/paper_to_theme_matrix.xlsx`).
