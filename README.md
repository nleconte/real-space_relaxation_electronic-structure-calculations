# Content

Also available in lammps/potential folder:
- [CBN_RPA.drip](./CBN_RPA.drip): DRIP parameters based on EXX-RPA DFT data for use with LAMMPS.  
- [CBN_LDA.drip](./CBN_LDA.drip): DRIP parameters based on LDA DFT data for use with LAMMPS. 
- [CH.rebo-LB](./CH.rebo-LB): Reparametrization of the CH.rebo file, for use with LAMMPS.

Input file:
- `lammps.in.gap2020`: input file for LAMMPS that leverages the gap2020 potential for intralayer interactions. Check [Quip interface for LAMMPS](https://lammps.sandia.gov/doc/pair_quip.html) as well as [some notes regarding installation](quipInstallation).

Output scripts:
- [getOutput.py](./getOutput.py) and [getOutputOnlyG.py](./getOutputOnlyG.py): extract data from LAMMPS `dump.minimization` file
- `getInterlayerDistace.py`: extract interlayer distances from files in previous step
- `getDisplacements.py`: extract displacements from files in first step

Scripts:
- [GenMoire.f90](./GenMoire.f90): script to create commensurate cells for tBG, aligned hBN/G, etc, with arbitrary precision on the twist angle when increasing the simulation cell
- [fracToCart.py](./fracToCart.py): script to go from fractional to cartesian coordinates (not my own script, credits given in header of script)
- [replaceFrac.py](./replaceFrac.py): script to replace the fractional coordinates by the cartesian coordinates in the `*.mol` file generated by the GenMoire.f90 script
- [prepareMol.sh](./prepareMol.sh): shell script to prepare the mol file using the GenMoire.f90 output using the two python scripts above
- Scripts to extract elastic constants from a LAMMPS calculation for hexagonal system

# Future content
Code:
- `Gendata.in`: input file to perform bandstructure calculation
- `grabnes`: binary to perform the bandstructure calculation
- Access to source code
 
