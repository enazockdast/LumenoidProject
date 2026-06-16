# Hypotheses

## H1: One Chiral Active-Gel Framework Spans 2D Rotation and 3D Spirals

Statement:

The collective dynamics of the cell layer — CCW rotation in the 2D planar colony and vortices/spirals on the 3D lumenoid — are different geometric expressions of the same chiral active polar/nematic gel. Flattening the sphere recovers the 2D rotating-monolayer limit; closing the flat layer onto a sphere introduces topological defects and curvature that reshape the same flow into vortices and spirals.

Prediction:

A single set of activity/chirality parameters should reproduce 2D rotation and 3D vortices/spirals; reversing chirality reverses both the 2D rotation sense and the 3D spiral handedness.

Evidence:

* The 3D solver reproduces aster/vortex/spiral regimes (active-gel theory; Kruse et al., 2004).
* CCW 2D rotation is robustly observed; the flat-geometry limit of this model has not yet been run.

Confidence:

Medium (unifying working hypothesis)

---

## H2: The 2D Planar Colony Shows Chiral CCW Rotation with a Size-Dependent Profile

Statement:

Before the 3D transition, the planar hiPSC colony exhibits coordinated, chirally biased (CCW) collective rotation driven by chiral active stress. The radial profile of angular velocity is set by edge effects and a screening length, so it depends on colony size.

Prediction:

The angular velocity ω(r) measured vs distance from the colony edge has a characteristic profile that rescales with colony size in the way the active-nematic model predicts (e.g. set by the ratio of colony radius to screening length). A net CCW bias is present.

Evidence:

* CCW collective motion during 2D colony formation is a robust preliminary observation.
* A label-free model for the ZSD-20× air objective enables brightfield nuclear tracking to measure ω(r) across colony sizes (planned).

Confidence:

Medium (robust observation; quantitative profile/size test pending)

---

## H3: On the Sphere, Incompressible Active Flow Gives Only Vortices (No Point-Source Spirals)

Statement:

The active/chiral stress on the closed shell drives a divergence-free (toroidal) tangential flow whose streamlines are closed loops about the +1 defects; it cannot, by itself, form spirals converging on or diverging from a point.

Prediction:

With no out-of-plane flux, projected streamlines are closed loops, surface divergence ∇_S·v ≈ 0, and an aster (radial polarity) drives essentially no flow.

Evidence:

* The Stokes solver reconstructs v from toroidal vector spherical harmonics only, which are divergence-free.
* A pure aster produces zero velocity to machine precision (the spheroidal force is annihilated by the toroidal projection).

Confidence:

High

---

## H4: 3D Spirals Require Out-of-Plane Nuclear Motion (INM) as a Source

Statement:

The observed spirals with point sources require a non-zero surface divergence, supplied by out-of-plane (radial) nuclear motion. Projected onto the shell this radial flux is a source/sink field s(θ,φ,t); the spiral is the superposition of the active toroidal swirl and the spheroidal radial in/outflow it induces.

Prediction:

Measured ∇_S·v is non-zero and localized at spiral cores; adding the source to the model reproduces the spiral streamline geometry.

Evidence:

* Lattice light-sheet streamlines show vortices/spiral cores over a heterogeneous speed field (preliminary).
* Continuity with a source gives v = ∇_S Φ, Δ_S Φ = s; the point-source Green's function v_θ = cot(θ/2)/(4πR) is reproduced to <10⁻³, and the coupled solver produces spiral-capable flow.
* Direct measurement of ∇_S·v at spiral cores is pending.

Confidence:

Medium (working hypothesis)

---

## H5: The Source Is Set by Mitosis / Cell-Cycle-Gated Nuclear Motion (INM)

Statement:

The out-of-plane nuclear flux is interkinetic nuclear migration — cell-cycle-controlled apical/basal nuclear movement, with mitosis the strongest radial event — so the effective source is concentrated at dividing cells and modulated by local cell-cycle phase.

Prediction:

Mitotic events coincide with transient radial (r-direction) nuclear motion and a local burst of streamline divergence; source strength (and spiral intensity) tracks the division rate. The planned 48-hour lattice light-sheet runs (>1 division) should resolve this mitosis↔streamline correlation.

Evidence:

* INM is a known, cell-cycle-gated, radial process in (pseudo)stratified epithelia; lumenoid cells become columnar/pseudostratified.
* Direct correlation of mitosis and radial motion with streamlines is the explicit aim of the 48-hour datasets (planned).

Confidence:

Low–Medium (to be tested)

---

## H6: Collective Dynamics Scale with Lumenoid Size R

Statement:

Lumenoid size R enters the model directly (screening ratio λ/R, the Stokes response ∝ ηl(l+1)/R²+Γ, the source Green's function ∝ 1/R), so the streamline pattern and speed should change in a predictable way as the lumenoid grows.

Prediction:

Tracking streamlines vs time — equivalently vs R — over the 48-hour runs should show the magnitude and structure of collective flow change with size as the model predicts, providing a near-parameter-free test.

Evidence:

* R appears explicitly in every term of the model.
* Time/size-resolved streamline series are the explicit aim of the planned datasets.

Confidence:

Medium (strong, direct test once data are in hand)

---

## H7: Perturbations Dissect the Drivers of Collective Motion

Statement:

Growth rate, mechanics, and ion transport can be separated by perturbation. Reducing growth lowers the growth-generated active stress; weakening tight junctions changes both mechanics and permeability.

Prediction:

* **Rapamycin** (reduced growth) reduces the magnitude of collective motion (slower rotation/vortices) and, via fewer divisions, weakens the INM source and the spirals.
* **TJP1 (ZO-1) knockdown** changes flow in coupled, non-trivial ways through both shell mechanics and permeability; **mosaic** knockdown (tunable % of expressing cells) reveals how a fraction of locally perturbed cells reorganizes the global collective motion and defect arrangement.

Evidence:

* Growth-rate and TJP1 effects are established for lumenoid growth (sibling project); their effect on collective dynamics is the aim of the planned perturbed lattice light-sheet runs.

Confidence:

Low–Medium (planned)

---

## H8: Collective Dynamics Are Coupled to Cell Shape and the 2D→3D Transition

Statement:

The collective flow and the cell-shape program co-evolve: the flat→columnar/pseudostratified shape change and the closure of the layer into a sphere alter (and are altered by) the collective dynamics.

Prediction:

Onset/clearing of CCW rotation correlates with the 2D→3D transition and with cell-height/aspect-ratio changes; shape perturbations change the flow regime, and flow perturbations change shape.

Evidence:

* Cells are measurably taller (columnar) in lumenoids than in flat colonies.
* The causal coupling is not yet modeled or tested.

Confidence:

Low (to be developed)

---

## H9: Substrate Traction, Not Active Stress Divergence, Is the Dominant Active Driving Force in Confluent Epithelia

Statement:

In substrate-bound confluent epithelia, cell–substrate traction — the monopolar body force **f** = γv₀**p** arising from self-propulsion of cells along their polarity — dominates the dipolar active stress divergence −∇_S(ζ**p**⊗**p**). This changes the mechanism by which polarity drives collective flow: the monopolar force is nonzero everywhere **p** is nonzero (including the far field away from defects), while the dipolar term is large only near defects and polarity gradients.

Prediction:

* A traction-dominant model reproduces the observed flow magnitudes and patterns without requiring the dipolar stress as a leading-order contribution.
* On dimensional grounds, the monopolar force beats the dipolar term by a factor L/ℓ (system size over polarity-variation length) at large scales, so the traction term dominates in well-ordered polarity states.
* Blocking substrate adhesion (reducing γ) should weaken collective flow more than blocking myosin contractility (which reduces ζ), if traction dominates.

Evidence:

* Traction-force and stress microscopy of confined MDCK monolayers (Pricoupenko et al. 2024) shows active stresses are subdominant compared with traction forces; collective rotation is set primarily by traction.
* Spreading monolayer theory (Blanch-Mercader & Casademunt 2017): substrate traction localized at polarized edge cells controls tissue-scale kinematics.
* The monopolar body force f = γv₀p is implemented as the default in the solver; it requires no surface derivatives of p, making the geometric complexity reside entirely in the Stokes inversion.

Confidence:

Medium–High (supported by literature; direct test via adhesion perturbation pending)

---

## Methods note: Quantitative Conclusions Require the Corrected IMEX Formulation

Trustworthy flow predictions require the corrected surface Laplacian (diffusive Frank force) and the IMEX (implicit-Frank) integration; the earlier explicit, sign-inverted scheme was unstable (velocities diverged) while a scale-invariant diagnostic could still appear to "pass." The corrected scheme is bounded, convergent, and passes the full validation suite (9/9).
