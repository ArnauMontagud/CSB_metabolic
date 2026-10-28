# Running the metabolic practical on your own machine

Not needed for class, the Binder link in the README gives you the same thing.

## With conda

```bash
conda env create -f environment.yml
conda activate CSB
jupyter lab practical_metabolic.ipynb
```

## With pip and a virtual environment

```bash
python3 -m venv cbm
source cbm/bin/activate          # Windows: cbm\Scripts\activate
pip install cobra swiglpk jupyterlab
jupyter lab practical_metabolic.ipynb
```

## Problems seen before

| Symptom | Fix |
|---|---|
| `Solver not found` or `No LP solver available` | `conda install -c conda-forge glpk swiglpk` inside the environment |
| SBML warnings about `OBJECTIVE_COEFFICIENT in KineticLaw` when loading iJO1366 | Harmless, the model loads fine |
| Loading iJO1366 takes very long | Normal the first time, about 2 seconds after that |
| `single_gene_deletion` very slow | Expected, it is 1367 optimisations. Around 5 seconds for the whole genome on a normal laptop |
