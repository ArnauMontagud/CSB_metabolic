# CSB metabolic modelling practical

Hands-on material on constraint-based metabolic modelling (COBRA) for
**Computational Systems Biology** (42589), Master's in Bioinformatics, ETSE,
Universitat de Valencia. **Session 10.**

## The three practical sessions

| Session | Topic | Repository |
|---|---|---|
| S8 | Boolean modelling of signalling networks | [CSB_signalling](https://github.com/ArnauMontagud/CSB_signalling) |
| S9 | Cell-line specific models from omics data (PROFILE) | [CSB_personalisation](https://github.com/ArnauMontagud/CSB_personalisation) |
| **S10** | Constraint-based metabolic modelling and FBA | [CSB_metabolic](https://github.com/ArnauMontagud/CSB_metabolic) |

All three are listed with their launch badges at
[CSB_course_UV](https://github.com/ArnauMontagud/CSB_course_UV).

## Run it in your browser

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ArnauMontagud/CSB_metabolic/HEAD?urlpath=lab/tree/practical_metabolic.ipynb)

Click the badge. Nothing to install. First launch of the day takes a few minutes,
later ones about half a minute.

- **Binder keeps nothing.** `File > Download` your notebook as soon as you start,
  and again at the end. The copy you download is what you hand in.
- **Ten minutes without activity closes your session.** Download before the break.

## What is in here

| File | What it is |
|---|---|
| `practical_metabolic.ipynb` | The notebook used in class: three hands-on blocks and four evaluated exercises |
| `data/m9_invivo_lethals.*` | Genes found to be essential experimentally on M9 glucose minimal medium |
| `data/argonne_invivo_lethals.*` | The same, for a rich medium |
| `data/argonne_media.*` | The rich medium of that experiment, in the identifiers of the original study |
| `data/rich_medium.json` | The same medium, ready to assign to `model.medium`, built from the file above |
| `environment.yml` | The exact software versions, tested |
| `INSTALL.md` | How to run it on your own machine instead |

The genome-scale model of *E. coli*, iJO1366 (2583 reactions, 1367 genes), is not a file
here: it ships with COBRApy and the notebook loads it with `cobra.io.load_model`.

## What the notebook covers

**Hands-on 1.** Building a stoichiometric model from scratch, the stoichiometric matrix,
a first FBA, why the optimum need not be unique (flux variability), and the same steps on
a genome-scale model, including a change of growth medium.

**Hands-on 2.** Single and genome-wide gene knock-outs, validated against experimental
essentiality data with a confusion matrix, and what the errors are made of.

**Hands-on 3.** Metabolic engineering: production envelopes and coupling succinate
production to growth.

## Credits

Material mainly developed by Miguel Ponce de Leon (Barcelona Supercomputing
Center) and adapted by Arnau Montagud (I2SysBio, CSIC-UV).

## References

1. Orth JD et al. (2011) A comprehensive genome-scale reconstruction of *Escherichia coli*
   metabolism, 2011. *Mol Syst Biol* 7:535. [doi:10.1038/msb.2011.65](https://doi.org/10.1038/msb.2011.65)
2. Ebrahim A, Lerman JA, Palsson BO, Hyduke DR (2013) COBRApy. *BMC Syst Biol* 7:74.
   [doi:10.1186/1752-0509-7-74](https://doi.org/10.1186/1752-0509-7-74).
   Documentation: <https://cobrapy.readthedocs.io/>
3. Orth JD, Thiele I, Palsson BO (2010) What is flux balance analysis? *Nat Biotechnol*
   28:245-248. [doi:10.1038/nbt.1614](https://doi.org/10.1038/nbt.1614)
