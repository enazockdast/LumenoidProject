# Cell Sorting Experiment-Modeling Roadmap

## Program Goal

Build a quantitative theory for how time-dependent adhesion, contractility,
motility, proliferation, and cell-state signaling control cell sorting in
lumenoids.

The program progresses from global control of mechanical parameters to local
signaling-mechanics feedback:

```text
dynamic global control
    -> independent control of adhesion and contractility
    -> local signaling-dependent mechanical control
```

## Aim 1: Dynamic Control Of N-Cadherin-Mediated Sorting

### 1.1 Measure Induction And Washout Kinetics

Use the existing DOX-inducible N-cadherin line in lumenoids. Begin with simple
induction and washout experiments before interpreting sorting outcomes.

Vary:

- DOX concentration;
- induction duration;
- time of DOX addition;
- time of DOX removal.

Estimate:

- delay between DOX addition and N-cadherin expression;
- time required to reach steady expression;
- decay time following DOX removal;
- dependence of response times on dose and induction duration.

The fluorescent reporter can provide a high-throughput expression proxy.
Selected time points should directly measure membrane-localized N-cadherin.

Fit a minimal response model:

```text
dN/dt = k_on f(C_DOX) - k_off N
```

### 1.2 Test Reversibility Of Sorted Domains

Allow mixed-cell lumenoids to sort under DOX, then remove DOX:

- before substantial sorting;
- after partial sorting;
- after mature domains form;
- continuously induced and uninduced controls;
- sham-wash controls.

Primary question:

```text
sorted state
    -- remove induced interaction difference -->
mixed state, slowly relaxing state, or persistent state?
```

### 1.3 Model Time-Dependent Adhesion

Introduce a dynamic adhesion state for induced cells using the measured
induction and removal kinetics. Sweep adhesion strength, turnover time,
motility, proliferation, and tissue fluidity.

Classify regimes:

- rapid remixing;
- slow domain dissolution;
- interface roughening without complete remixing;
- persistent mechanically trapped domains.

### Aim 1 Measurements

- membrane N-cadherin intensity;
- sorting index and heterotypic-contact fraction;
- domain-interface length and domain-size distribution;
- neighbor-exchange rate;
- cell mean-squared displacement and effective diffusivity;
- pattern autocorrelation time;
- lumenoid size, shape, and integrity.

## Aim 2: Dynamic Control Of Actomyosin Contractility

### 2.1 Confirm Feasible Inducible Perturbations

Ask the experimental team to evaluate DOX-controlled perturbations of:

- `ROCK1`;
- `MYH9`, encoding non-muscle myosin-IIA;
- `MYH10`, encoding non-muscle myosin-IIB.

`ROCK1` is the closest match to the existing inducible CRISPR-interference
infrastructure and has already been discussed as a sorting perturbation.
`MYH9` and `MYH10` provide more direct perturbations of force-generating
myosin-II isoforms, but may present greater risks to division, survival, and
lumenoid integrity.

Initial selection criteria:

- induction and washout are measurable and sufficiently reversible;
- lumenoids remain viable and structurally intact;
- the perturbation produces a measurable mechanical phenotype;
- effects on proliferation and motility can be quantified.

### 2.2 Compare Adhesion And Contractility Perturbations

Apply matched induction and washout protocols to N-cadherin and the selected
contractility perturbation.

Determine whether differential contractility:

- generates sorting independently;
- accelerates or inhibits adhesion-driven sorting;
- alters interface sharpness and domain morphology;
- changes tissue fluidity;
- changes reversibility of established patterns.

### 2.3 Model Contractility Independently From Adhesion

In the center-based model, represent contractility through active cell-scale
forces or an effective cortical-tension parameter. In the vertex/Voronoi model,
represent it through junctional edge tension:

```text
E = E_adhesion + sum_over_edges Lambda_ij(t) l_ij
```

The initial model should vary adhesion and contractility independently, while
the interpretation of experiments should allow each perturbation to affect
motility, fluidity, and proliferation as measured.

## Aim 3: Couple Cell-Cell Signaling To Mechanical Properties

### 3.1 Computational Phase

Implement neighbor-dependent fate dynamics and compare models in which fate
controls:

1. homotypic adhesion;
2. heterotypic adhesion;
3. both homotypic and heterotypic adhesion;
4. contractility;
5. motility;
6. adhesion and contractility together.

Map pattern class and stability as functions of:

- signaling and fate-commitment timescales;
- neighbor-exchange rate;
- homotypic-to-heterotypic interaction ratio;
- contractility contrast;
- motility and proliferation.

### 3.2 Experimental Phase

Once cell-contact signaling and programmable mechanical tools are available,
test whether local regulation can:

- generate and maintain salt-and-pepper organization;
- stabilize or destabilize heterotypic contacts;
- produce persistent domains or stripes;
- repair patterning defects after rearrangement.

Independent control of `J_AA`, `J_BB`, and `J_AB` will likely require
programmable synthetic adhesion molecules rather than natural cadherins alone.

## Immediate Sequence

1. Measure N-cadherin induction and washout kinetics in lumenoids.
2. Remove DOX after partial and mature sorting to test pattern reversibility.
3. Fit and validate a time-dependent adhesion model.
4. Confirm feasibility and status of inducible `ROCK1`, `MYH9`, and `MYH10`
   perturbations.
5. Select one contractility perturbation for matched adhesion-versus-tension
   experiments.
6. Add independent adhesion and edge-tension control to the lumenoid model.
7. Add signaling-dependent fate and mechanics computationally.
8. Progress toward experimental cell-contact-dependent mechanical regulation.

## Near-Term Deliverable

A quantitative determination of whether sorted lumenoid domains persist,
dissolve, or reorganize after the induced mechanical asymmetry is removed,
together with a model explaining the observed response in terms of protein
turnover and tissue fluidity.
