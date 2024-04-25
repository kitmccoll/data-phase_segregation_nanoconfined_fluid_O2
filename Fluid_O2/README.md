## Nanoconfined fluid O<sub>2</sub>
This folder contains a two Jupyter Notebook, which plot Figures 4a, b, and c in the manuscript. Data comes from two AIMD trajectory files; one representing the cathode material (MnO<sub>0.8</sub>O<sub>2</sub>) after charging, and one of a box of O<sub>2</sub> molecules. 
- `Fig_4ab_RDFs.ipynb` reads the two AIMD trajectory files and uses the [`vasppy`](https://github.com/bjmorgan/vasppy) code to calculate radial distribution functions for several differnt atom pairs.
- `Fig_4c_O2_Li_O_ion_MSD` uses the [`kinisi`](https://github.com/bjmorgan/kinisi) code (see publication in: [JOSS](https://joss.theoj.org/papers/10.21105/joss.05984)) to calculate the mean squared displacements of atoms and ions in the structure.
- Data is contained in `../Data/Data_fluid_O2/`
