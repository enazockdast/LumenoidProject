# Cell Sorting Status

## Current Experimental Capability

### Demonstrated Or In Progress

- DOX-inducible N-cadherin expression is available in hiPSCs.
- Multiple N-cadherin-expression clones span low, medium, and high expression.
- N-cadherin induction produces measurable sorting or patterning in two-
  dimensional colonies and spheroids.
- Spheroid data comparing control and DOX-induced N-cadherin conditions are
  being generated.
- Full-length N-cadherin is currently the most reliable positive control for
  adhesion-driven sorting.
- Synthetic adhesion constructs and full-length cadherins have been screened in
  hiPSC colonies.

### Proposed But Not Yet Demonstrated

- Dynamic N-cadherin washout experiments after sorting.
- Quantitative measurement of N-cadherin induction and removal timescales.
- A DOX-inducible contractility perturbation validated for lumenoids.
- Cell-contact-dependent signaling that changes adhesion or contractility.
- A closed-loop lateral-inhibition-mechanics experiment.

## Current Modeling Capability

- Stable explicit agent-based models exist for spheroids, flat monolayers, and
  lumenoids.
- Current models include adhesion, motility, proliferation, polarity, and
  bending rigidity.
- Simulations can vary homotypic and heterotypic adhesion and can be run fast
  enough for parameter sweeps.
- Proliferation changes simulated cell motion and tissue fluidity.
- Differential adhesion and contractility through an edge-tension term are
  being incorporated into a dual-Voronoi/vertex formulation.

## Working-Group Priorities

The current plan is aligned with Cell Sorting Working Group discussions:

- explore phase diagrams across adhesion, motility, proliferation, and
  contractility;
- focus more strongly on three-dimensional lumenoid sorting;
- compare experimental and simulated cell motion and neighbor exchange;
- couple lateral inhibition to adhesion or motility in simulation;
- test whether signaling and mechanics act on compatible timescales.

## Contractility Perturbation Candidates

| Candidate | Rationale | Main interpretation risk |
|---|---|---|
| `ROCK1` repression | Existing inducible CRISPR-interference precedent; upstream control of actomyosin activity | Also changes motility, adhesion maturation, polarity, and survival |
| `MYH9` repression | Directly reduces non-muscle myosin-IIA force generation | May disrupt junctions, migration, cytokinesis, and viability |
| `MYH10` repression | Tests non-muscle myosin-IIB-dependent tension and force persistence | May alter polarity, persistent force transmission, and tissue organization |
| Vimentin induction | Changes stiffness and force transmission through a distinct mechanism | Not a direct or isolated contractility perturbation |
| Rho-pathway activation | Can increase actomyosin activity | Broad, potentially strong, and difficult to interpret |
| Shroom2-based control | Can drive localized constriction | Strongly coupled to shape and polarity changes |

The immediate decision is whether `ROCK1`, `MYH9`, or `MYH10` can be placed
under a sufficiently tunable and reversible DOX-controlled perturbation without
compromising lumenoid integrity.

## Key Scientific Risks

- N-cadherin abundance may not map monotonically to a single effective adhesion
  energy.
- Cadherin and synthetic-adhesion perturbations may also change contractility,
  motility, and endogenous adhesion proteins.
- `ROCK1`, `MYH9`, and `MYH10` perturbations are not pure contractility knobs.
- Reporter fluorescence may not accurately report membrane-localized
  N-cadherin.
- Washout may be limited by slow protein turnover rather than tissue mechanics.
- Proliferation may change both tissue fluidity and cell-population ratios.

## Immediate Decisions And Actions

1. Narrow the first dynamic-control study to lumenoids.
2. Define a minimal DOX induction/washout matrix.
3. Measure reporter dynamics and membrane N-cadherin at selected time points.
4. Establish partial-sorting and mature-sorting washout conditions.
5. Add time-dependent adhesion to the lumenoid simulation.
6. Ask the experimental team about feasibility and current status of inducible
   `ROCK1`, `MYH9`, and `MYH10` perturbations.
7. Select measurements that distinguish adhesion, contractility, motility, and
   proliferation effects.
