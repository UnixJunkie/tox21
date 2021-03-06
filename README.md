# Tox21

My copy of the Tox21 dataset.

# Data source

https://github.com/deepchem/deepchem/tree/master/datasets/tox21.csv

download date: 09/11/2018 at 13:59:05

# Preparation protocol

All smiles strings (molecules) have been standardised using

https://github.com/flatkinson/standardiser

Molecules that did not pass standardisation have been removed.
Cf. standardisation/errors.smi for such molecules.

All molecules tested on a given toxicity endpoint/target were copied
into a specific directory for that target.
All toxic molecules for a given target have had their name prefixed
with the word "active".
Each list of molecules was randomized.

# Directory structure

```
tox21.csv: backup copy of the original data source

targets.txt: list of all toxicity endpoints in the dataset; one per line.
             Target names are in the same order than columns
             in the tox21.csv file.

TARGET/ligands_std_rand.smi: all toxic molecules for TARGET and all
                             non toxic molecules; in random order

standardisation/errors.smi: molecules that did not pass standardisation
standardisation/standardised.smi: molecules that passed standardisation
```
# Bibliography

```
@article{Huang2016,
author = {Huang, Ruili and Xia, Menghang and Nguyen, Dac-Trung and Zhao, Tongan and Sakamuru, Srilatha and Zhao, Jinghua and Shahane, Sampada A. and Rossoshek, Anna and Simeonov, Anton},
title = {Tox21Challenge to Build Predictive Models of Nuclear Receptor and Stress Response Pathways as Mediated by Exposure to Environmental Chemicals and Drugs},
journal = {Frontiers in Environmental Science},
volume = {3},
pages = {85},
year = {2016},
doi = {10.3389/fenvs.2015.00085},
}
```
