# Cell Sorting Hypotheses

## H1: Sorted Domains Can Retain Mechanical Memory

After N-cadherin-induced sorting, removal of DOX will eliminate the imposed
expression difference only after a finite turnover time. Once that difference
has decayed, the subsequent fate of the pattern will depend on tissue fluidity.

Predictions:

- Fluid lumenoids will remix after N-cadherin levels converge.
- Jammed lumenoids will retain long-lived domains after washout.
- Partial sorting will be more reversible than mature sorting.
- Domain persistence will correlate more strongly with neighbor-exchange rate
  than with the instantaneous sorting index.

Discriminating measurements:

- membrane-localized N-cadherin intensity;
- heterotypic-contact fraction and domain-interface length;
- neighbor-exchange rate and cell mean-squared displacement;
- pattern autocorrelation following washout.

## H2: Sorting Depends On Competing Timescales

Dynamic sorting is controlled by the relative rates of interaction-strength
change, cell rearrangement, proliferation, and domain coarsening:

```text
induction/removal timescale
vs. mechanical relaxation timescale
vs. neighbor-exchange timescale
vs. proliferation timescale
```

Predictions:

- Fast induction relative to rearrangement will initially create a mechanically
  heterogeneous but spatially mixed tissue.
- Slow protein removal relative to rearrangement will delay remixing after
  washout.
- Proliferation can fluidize the tissue and accelerate both sorting and
  remixing, while also changing cell-number ratios.

## H3: Differential Contractility Can Drive Or Reshape Sorting

Differences in cortical or junctional tension can generate sorting even when
adhesion is unchanged. They can also sharpen, roughen, or destabilize domains
created by differential adhesion.

Candidate global perturbations:

- `ROCK1` repression to reduce Rho-ROCK-mediated actomyosin activity;
- `MYH9` repression to reduce non-muscle myosin-IIA activity;
- `MYH10` repression to reduce non-muscle myosin-IIB activity.

Predictions:

- Contractility perturbations will alter interface geometry and tissue fluidity
  as well as sorting.
- `MYH9` and `MYH10` perturbations may produce distinct outcomes because the
  two myosin-II isoforms differ in force generation, localization, and
  timescale.
- Contractility-driven patterns will not generally be explained by changing a
  single effective adhesion parameter.

Important caveat:

These perturbations can also affect motility, polarity, adhesion maturation,
division, and survival. Their effects must be inferred from multiple dynamic
measurements rather than labeled as pure changes in contractility.

## H4: Signaling-Mechanics Feedback Can Stabilize New Pattern Classes

Neighbor-dependent signaling can assign cell fate, while fate controls
adhesion, contractility, or motility:

```text
neighbor identities
    -> signaling
    -> cell fate
    -> mechanical properties
    -> rearrangement and new neighbors
```

Predictions:

- Lateral inhibition coupled to heterotypic adhesion can stabilize
  salt-and-pepper-like organization.
- Excessively strong adhesion can trap signaling defects rather than repair
  them.
- Coupling fate to contractility can create boundary sharpening, extrusion, or
  dynamic remodeling not obtained from adhesion alone.
- Pattern class and stability will depend on the ratio of signaling, fate
  commitment, and neighbor-exchange timescales.

## H5: Homotypic And Heterotypic Interactions Must Be Distinguished

Natural cadherin perturbations may change several entries of the effective
interaction matrix simultaneously and may also alter cortical mechanics:

```text
J_AA, J_BB, J_AB
```

Independent control of homotypic and heterotypic interactions will likely
require programmable synthetic adhesion molecules. Experiments should therefore
avoid interpreting construct identity as a direct measurement of one pairwise
interaction energy.
