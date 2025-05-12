This script run for solvent accessibility analysis with NACCESS and local interaction ΔΔG analysis with MutateX

Solvent accessibility analysis with NACCESS

1. activating the conda environment
```bash
conda activate /home/ctools/protein_structure_course
```
2. Run the NACCESS
5P9I PDB Structure
```bash
naccess 5P9I_No.pdb
```
6YYG PDB Structure
```bash
naccess 6YYG_A_clean.pdb
```
3. Extract the corresponding data
```bash
grep 28 6YYG_A_clean.rsa
grep 33 6YYG_A_clean.rsa
grep 113 6YYG_A_clean.rsa
grep 408 5P9I_No.rsa
grep 562 5P9I_No.rsa
grep 628 5P9I_No.rsa
grep 418 5P9I_No.rsa
grep 426 5P9I_No.rsa
grep 430 5P9I_No.rsa
grep 607 5P9I_No.rsa
grep 589 5P9I_No.rsa
grep 613 5P9I_No.rsa
grep 506 5P9I_No.rsa
```

