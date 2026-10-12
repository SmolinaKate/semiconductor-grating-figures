# Theory of deeply subwavelength electromagnetic structuring of semiconductors due to thermal-ionization instability — figures

Python notebooks that produce the figures for the paper *"Theory of deeply subwavelength electromagnetic structuring of semiconductors due to thermal-ionization instability"*.
Each notebook reproduces one figure and compares the analytical result with the FEM data.

## Structure

```
.
├── notebooks/                   # Jupyter notebooks (one per figure)
│   ├── Field.ipynb              # field map near the semiconductor surfac
│   ├── Grating1.ipynb           # dielectric grating: FEM vs Eq. (20)
│   └── Grating2.ipynb           # geometric corrugation: FEM vs Eq. (54)
├── data/                        # input data (FEM results)
│   ├── Field3.txt.gz            # field map z, x, |Ey|, ... (gzipped)
│   ├── e_complex.txt            # dielectric grating sweep
│   └── e_complex_g_no_gamma.txt # geometric corrugation sweep
└── README.md
```

## Run

```
pip install numpy matplotlib scipy jupyter
jupyter notebook notebooks/
```

Run the notebooks from inside the `notebooks/` folder (paths to `../data/` are relative).
Running a notebook regenerates its figure (`*.png`, `*.pdf`) in `../Figs/`.

## Data

`data/Field3.txt.gz` is a gzip-compressed text file; the notebook reads it directly with
`gzip.open(...)`. Decompress if needed: `gunzip -k data/Field3.txt.gz`.
