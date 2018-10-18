[![Build Status](https://travis-ci.org/kbsezginel/lammps_interface.svg?branch=master)](https://travis-ci.org/kbsezginel/lammps_interface)
# Modified LAMMPS Interface for pylmps
## Authors of the original code

-   Peter Boyd
-   Mohamad Moosavi
-   Matthew Witman

## to be blamed for the crippled version:

-   Rochus Schmid [RUB/MOF+]

## Description
This program was designed for easy interface between the crystallographic
information file (.[cif]) and the Large-scale Atomic Molecular Massively
Parallel Simulator ([Lammps]).

The modified version can not read a file anymore but gets a mol object (MOFplus/molsys) and creates
only UFF or UFF4MOF input for lammps with the pylmps wrapper.
NOTE: If you want to use this code for its orginal purpose use the original code. No reading of CIF files possible.

## Installation
Clone the repository, enter the directory and install dependencies by:
```
pip install -r requirements.txt
```

The Python module can be installed globally by:
```
python setup.py install
```

## Licence
MIT licence (see LICENCE file)

## Citation
The publication associated with this code is found here:

Boyd, P. G., Moosavi, S. M., Witman, M. & Smit, B. Force-Field Prediction of Materials Properties in Metal-Organic Frameworks. J. Phys. Chem. Lett. 8, 357–363 (2017).

dx.doi.org/10.1021/acs.jpclett.6b02532

[Lammps]: http://lammps.sandia.gov/
[cif]: https://en.wikipedia.org/wiki/Crystallographic_Information_File
