## Folding Free Energy Calculation (ΔΔG) with MutateX Ensemble Mode
This script run for Mutatex Ensemble mode

Run the CABS-flex to generate the ensembled structure 

1. Deactivate the conda environment
```bash
conda deactivate
```
2. Activate the CABS-flex evinronment
```bash
source /home/ctools/CABS/bin/activate
```
3. Run the simulation
for 5P9I structure
```bash
nohup CABSflex -i 5P9I_No.pdb -k 10 -y 50 -a 10 -v 3 -z 10 -A --log &
```
for 6YYG structure
```bash
nohup CABSflex -i 6YYG_A_clean.pdb -k 10 -y 50 -a 10 -v 3 -z 10 -A --log &
```

4. Self scan for the generated structure
```bash
nohup nohup mutatex model0_checked.pdb -p 4 -x /home/ctools/foldx/foldx -m mutation_list.txt -f suite5 -R repair_runfile_template.txt -M mutate_runfile_template.txt -c -L -l -v -s &
```
5. Copy the model from CABS-flex to directory
```bash
cp../model0_checked.pdb .
```
6. copy the template file for MutateX to the directory
```bash
cp /home/projects/22117_proteins_2025/lecture4/mutatex_templates/mutatex/templates/foldxsuite5/mutation_list.txt .
cp /home/projects/22117_proteins_2025/lecture4/mutatex_templates/mutatex/templates/foldxsuite5/repair_runfile_template.txt .
cp /home/projects/22117_proteins_2025/lecture4/mutatex_templates/mutatex/templates/foldxsuite5/mutate_runfile_template.txt .
```
7. Activate conda environment
```bash
conda activate /home/ctools/protein_structure_course/
```
8. Run MutateX
nohup mutatex model0_checked.pdb -p 3 -x /home/ctools/foldx/foldx -m mutation_list.txt -q poslist.txt -f suite5 -R repair_runfile_template.txt -M mutate_runfile_template.txt -c -L -l -v  &
