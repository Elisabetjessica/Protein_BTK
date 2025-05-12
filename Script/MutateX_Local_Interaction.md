## Solvent Accessibility Analysis with NACCESS and Folding Free Energy Calculation (ΔΔG) with MutateX
This script run for solvent accessibility analysis with NACCESS and folding free energy (ΔΔG) analysis with MutateX simple mode

Solvent accessibility analysis with NACCESS

1. activate the conda environment
```bash
conda activate /home/ctools/protein_structure_course
```
2. Run NACCESS
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

Folding free energy (ΔΔG) calculation with MutateX simple mode

1. Copy the necessary templates file to the working directory
```bash
cp /home/projects/22117_proteins_2025/lecture4/mutatex_templates/mutatex/templates/foldxsuite5/repair_runfile_template.txt .

cp /home/projects/22117_proteins_2025/lecture4/mutatex_templates/mutatex/templates/foldxsuite5/mutate_runfile_template.txt .

cp /home/projects/22117_proteins/lecture5_exercise/mutatex_templates/mutatex/templates/mutation_list.txt .
```
2. create a target mutation list, poslist.txt
```bash
nano poslist.txt
```
the content of the poslist
a. For 6YYG_A_clean.pdb
RA28
TA33
VA113
b. For 5P9I_No.pdb
LA408
RA562
TA628
YA418
DA426
KA430
AA607
EA589
GA613
CA506

3. Run MutateX
for 5P9I
```bash
nohup mutatex 5P9I_No.pdb -p 1 -m mutation_list.txt -x /home/ctools/foldx/foldx -f suite5 -R repair_runfile_template.txt -M  mutate_runfile_template.txt -q poslist.txt -L -l -v -C none &
```
for 6YYG
```bash
nohup mutatex 6YYG_A_clean.pdb -p 1 -m mutation_list.txt -x /home/ctools/foldx/foldx -f suite5 -R repair_runfile_template.txt -M  mutate_runfile_template.txt -q poslist.txt -L -l -v -C none &
```

4. Extract the result as a csv file
for 5P9I
```bash
ddg2excel -p 5P9I_No.pdb -l mutation_list.txt -q poslist.txt -d results/mutation_ddgs/2XWRA_noHOH_model0_checked_Repair/ -F csv
```
for 6YYG
```bash
ddg2excel -p 6YYG_A_clean.pdb -l mutation_list.txt -q poslist.txt -d results/mutation_ddgs/2XWRA_noHOH_model0_checked_Repair/ -F csv
```

