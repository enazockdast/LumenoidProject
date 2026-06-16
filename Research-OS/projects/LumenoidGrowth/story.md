## Reviewer Attack Surface

High Risk:
- Cell incompressibility assumption
- Parameter identifiability

Medium Risk:
- Homogeneous shell mechanics
- Constant material properties

Low Risk:
- Rapamycin validation
- ZO-1 discriminating experiment
# Story

## One-Sentence Claim

Lumenoid thickening emerges from a physical competition between cell growth, osmotic lumen expansion, and mechanical relaxation of the epithelial shell.

---

## The Puzzle

Many lumenized tissues and organoids become thinner as lumen pressure increases.

However, hiPSC lumenoids display the opposite behavior:

* Lumenoid radius increases over time.
* Epithelial thickness also increases.
* Thickness growth scales with lumenoid growth.

Why does a growing pressurized lumen not thin the epithelial shell?

---

## Central Idea

Cell growth continuously increases the total volume of the epithelial monolayer.

If osmotic lumen expansion and mechanical relaxation cannot keep pace with growth, compressive stresses develop within the shell.

Because cells are approximately incompressible, area compression is converted into increased epithelial thickness.

Thickening is therefore not an independent biological program but an emergent consequence of growth, transport, and mechanics.

---

## Minimal Physical Model

The model contains only three essential processes:

1. Cell growth

   * increases total cell volume

2. Osmotic transport

   * active ion pumping
   * passive ion leakage
   * water transport

3. Shell mechanics

   * epithelial elasticity
   * basement membrane mechanics
   * active tensions

Together these determine the dynamics of:

* inner radius
* outer radius
* shell thickness

---

## Key Prediction 1

Thickness should increase when cell growth outpaces osmotic and elastic relaxation.

Prediction:

Faster growth → thicker lumenoids

Slower growth → thinner lumenoids

---

## Test 1: Rapamycin

Question:

Does reducing growth reduce thickening?

Observation:

Rapamycin decreases growth rate and produces thinner lumenoids.

Result:

Without changing any other parameters, the model correctly predicts the reduction in thickness.

Interpretation:

Growth rate is a primary determinant of thickening.

---

## Key Prediction 2

The response to altered ion permeability should distinguish between weak and strong osmotic-flow regimes.

Weak-flow regime:

Changing permeability produces relatively small effects.

Strong-flow regime:

Increasing permeability dramatically reduces lumen size and increases thickening.

---

## Test 2: TJP1 (ZO-1) Perturbation

Question:

Which osmotic regime governs lumenoid growth?

Observation:

Increasing permeability through ZO-1 knockdown causes:

* shrinking lumen radius
* reduced outer radius
* increased shell thickness

Result:

These behaviors are quantitatively consistent with the strong osmotic-flow regime.

Interpretation:

Lumenoid growth is controlled by strong osmotic transport.

---

## Strongest Evidence

1. Model simultaneously explains inner radius, outer radius, and thickness.

2. Rapamycin predictions emerge by changing only the measured growth rate.

3. ZO-1 perturbations provide a discriminating test between competing physical regimes.

4. Control and perturbation datasets are explained within a single framework.

---

## Weakest Link

The model assumes:

* approximate cell incompressibility
* constant material properties
* homogeneous shell mechanics

Direct experimental validation of these assumptions remains incomplete.

Single-cell analyses are needed to test these assumptions.

---

## What Reviewers Will Ask

1. Is cell volume truly conserved during thickening?

2. Are mechanical properties constant throughout growth?

3. Could active remodeling explain thickening without compression?

4. How general is this mechanism across lumenized tissues?

5. Are parameter values uniquely identifiable?

---

## Broader Significance

This work provides a predictive mechanistic framework linking:

* tissue growth
* epithelial mechanics
* hydraulic transport

The results suggest that epithelial thickening can emerge as a generic physical consequence of growth in confined lumenized tissues.

More broadly, the work establishes how growth, transport, and mechanics can be integrated into explanatory models of morphogenesis.

