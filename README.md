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

which analyse and plot key data in Figure 2, 3 and 4 in the manuscript. The repositories will also cover all the analysis of DFT calculations, ab initio molecular dynamics simulations and cluster expansion and Monte Carlo simulations presented in the main paper, as well as the preparatory calculations peformed in to obtain structures with which to train the cluster expansion. Each section consits of annotated Jupyter notebooks that show how the computational analysis in the paper was conducted from calculation data.

Rerunning this workflow requires the raw calculation data files for several hundred DFT claculations, and AIMD trajectory files, which are not included in this repository due to a lack of space; data to generate key figures in the manuscript has been collated into `.json` files in the `./Data/` folder. 

A fully functional version will be available on the Bath University Research Archive [awaiting DOI], and [Zenodo]([![DOI](https://zenodo.org/badge/772626463.svg)](https://zenodo.org/doi/10.5281/zenodo.11068468))


