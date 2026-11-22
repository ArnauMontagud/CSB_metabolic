# Running the metabolic practical on your own machine

Not needed for class, the Binder link in the README gives you the same thing.

## With conda

```bash
conda env create -f environment.yml
conda activate CSB
jupyter lab practical_metabolic.ipynb
```

This is the tested route. Every version in `environment.yml` is pinned, so you get the
same environment as in class.

## With pip and a virtual environment

```bash
python3 -m venv cbm
source cbm/bin/activate          # Windows: cbm\Scripts\activate
pip install "cobra==0.32.1" "pandas==2.3.3" "matplotlib==3.11.2" jupyterlab
jupyter lab practical_metabolic.ipynb
```

Not tested every year. If something behaves oddly, use conda.

## Problems seen before

| Symptom | Fix |
|---|---|
| `Solver not found` or `No LP solver available` | `conda install -c conda-forge glpk swiglpk` inside the environment |
| The first `load_model("iJO1366")` is slow | Normal the first time, about 2 seconds afterwards. The model ships with COBRApy, so it does not download anything |
| `single_gene_deletion` seems stuck | Expected, it is 1367 optimisations. About 6 seconds for the whole genome |
| `FileNotFoundError: out/toymodel.sbml` | Run it from the repository folder, which contains `out/` and `data/` |
