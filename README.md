# CSB metabolic modelling practical

Hands-on material on constraint-based metabolic modelling (COBRA) for
**Computational Systems Biology** (42589), Master's in Bioinformatics, ETSE,
Universitat de Valencia. Session 10.

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
| `practical_metabolic.ipynb` | The notebook used in class, parts 1 to 5 |
| `data/iJO1366.xml` | Genome-scale model of *E. coli*, 2583 reactions, 1367 genes |
| `data/*_invivo_lethals.*` | Experimental essential genes, for validating predictions |
| `data/argonne_media.*` | Medium compositions |
| `environment.yml` | The exact software versions, tested |
| `INSTALL.md` | How to run it on your own machine instead |

## What the notebook covers

1. Building a toy metabolic model from scratch with COBRApy
2. Loading and inspecting the genome-scale model
3. Flux balance analysis
4. Single and systems-wide gene knock-outs, validated against in vivo data
5. Metabolic engineering design

## Credits

Material mainly developed by Miguel Ponce de Leon (Barcelona Supercomputing
Center) and adapted by Arnau Montagud (I2SysBio, CSIC-UV).

COBRApy: Ebrahim A, Lerman JA, Palsson BO, Hyduke DR (2013), *BMC Systems
Biology* 7:74, [doi:10.1186/1752-0509-7-74](https://doi.org/10.1186/1752-0509-7-74).
Documentation: <https://cobrapy.readthedocs.io/>
