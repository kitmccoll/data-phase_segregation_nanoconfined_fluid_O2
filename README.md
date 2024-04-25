# Data analysis for &ldquo;Phase segregation and nanoconfined fluid O<sub>2</sub> in a lithium-rich oxide cathode &rdquo;
Scripts to analyse and plot data supporting: Phase segregation and nanoconfined fluid O<sub>2</sub> in a lithium-rich oxide cathode ([ChemRxiv](https://chemrxiv.org/engage/chemrxiv/article-details/65b261ab9138d23161b931bd)).

Authors:
- Kit McColl (orcid: [0000-0002-7794-8276](https://orcid.org/0000-0002-7794-8276)) 
- Samuel W. Coles (orcid: [0000-0001-9722-5676](https://orcid.org/0000-0001-9722-5676))
- Pezhman Zarabadi-Poor
- Benjamin J. Morgan (orcid: [0000-0002-3056-8233](https://orcid.org/0000-0002-3056-8233))
- M. Saiful Islam (orcid: [0000-0002-3056-8233](https://orcid.org/0000-0003-0373-116X))

## Summary
This repository contains the analysis and figure-plotting workflow for the manuscript &ldquo;Phase segregation and nanoconfined fluid O<sub>2</sub> in a lithium-rich oxide cathode &rdquo; ([ChemRxiv](https://chemrxiv.org/engage/chemrxiv/article-details/65b261ab9138d23161b931bd)).

The workflow here contains three main components: 
- `Kinetics` (Kinetically possible rearrangements: AIMD)
- `Thermodynamics` (Thermodynamically favoured structures: cluster expansion & Monte Carlo)
- `Fluid_O2` (Nanconfined fluid O<sub>2</sub>)

which cover all the analysis of DFT calculations, ab initio molecular dynamics simulations and cluster expansion and Monte Carlo simulations presented in the main paper, as well as the preparatory calculations peformed in to obtain structures with which to train the cluster expansion. Each section consits of annotated Jupyter notebooks that show how the computational analysis in the paper was conducted from calculation data. The notebooks generate data-based Figures in the manuscript. 

Rerunning this workflow requires the raw calculation data files for several hundred DFT claculations, and AIMD trajectory files, which are not included in this repository due to a lack of space; data to generate key figures in the manuscript has been collated into `.json` files in the `./Data/` folder. 

A fully functional version is provided on the Bath University Research Archive [awaiting DOI], and [Zenodo](https://chemrxiv.org/engage/chemrxiv/article-details/65b261ab9138d23161b931bd) (doi: ??) ** update link **

## Kinetically possible rearrangements: AIMD
This folder contains two Jupyter Notebooks, which plot Figures 2a and 2b in the manuscript. 
- `Fig_2a_AIMD_rearrangements_energy.ipynb`, plots the total energy from a PBE+U AIMD trajectory as a function of time.
- `Fig_2d_HSE06_structural_relaxations_from_AIMD.ipynb`, plots the total energy from a series of structures that were extracted from the AIMD trajectory, and fully relaxed with the HSE06 hybrid DFT functional. 

## Thermodynamically favoured structures: cluster expansion & Monte Carlo
This folder contains two Jupyter Notebooks, which plots Figures 3a and 3d in the manuscript. 
- `Fig_3a_convex_hull.ipynb`, plots the formation energies for a series of 775 HSE06 calculations of structures along the O<sub>2</sub>–MnO<sub>2</sub>–MnO tie-line.
- `Fig_3d_O_envs.ipynb`, reads two structural files, and plots the frequency of their O–ion local environments. The two structure files are i) the pristine 'ribbon' superstructure and ii) a structure generated from the cluster-expansion driven Monte Carlo simulations. 

## Nanoconfined fluid O<sub>2</sub>
This folder contains a two Jupyter Notebook, which plot Figures 4a, b, and c in the manuscript. Data comes from two AIMD trajectory files; one representing the cathode material (MnO<sub>0.8</sub>O<sub>2</sub>) after charging, and one of a box of O<sub>2</sub> molecules. 
- `Fig_4ab_RDFs.ipynb` reads two AIMD 
- The notebook reads an AIMD trajectory file, and uses the [`vasppy`](https://github.com/bjmorgan/vasppy) code to calculate radial distribution functions, and the [`kinisi`](https://github.com/bjmorgan/kinisi) code (see publication in: [JOSS](https://joss.theoj.org/papers/10.21105/joss.05984)) to calculate the mean squared displacements of ions in the structure. 

