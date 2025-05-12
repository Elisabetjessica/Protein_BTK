## Binding Free Energy Calculation (ΔΔG) with MutateX

This script run for MutateX for Binding free energy calculation 

1. Activate conda environment
```bash
conda activate /home/ctools/protein_structure_course
```

2. Copy the necessary template for running the binding energy calculation
```bash
cp /home/projects/22117_proteins_2025/lecture4/mutatex_templates/mutatex/templates/foldxsuite5/repair_runfile_template.txt .

cp /home/projects/22117_proteins_2025/lecture4/mutatex_templates/mutatex/templates/foldxsuite5/mutate_runfile_template.txt .

cp /home/projects/22117_proteins/lecture5_exercise/mutatex_templates/mutatex/templates/mutation_list.txt .

cp /home/projects/22117_proteins/lecture5_exercise/mutatex_templates/mutatex/templates/interface_runfile_template.txt .
```

3. Create a poslist.txt for the target mutation

```bash
nano poslist.txt
```
4. Fill the poslist.txt with targeted residues
the content of the poslist
a. For 6YYG_WASP.pdb
RA28
TA33
VA113
b. For BTKPRK.pdb
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

5. Run the MutateX for the respective pdb file
for the 6YYG-WASP pdb structure
```bash
nohup mutatex 6YYG_WASP.pdb -p 4 -m mutation_list.txt -x /home/ctools/foldx/foldx -f suite5 -R repair_runfile_template.txt -M mutate_runfile_template.txt -q poslist.txt -L -l -v -C  none -B  -I interface_runfile_template.txt &
```
 
for the 5P9I-PRKCQ pdb structure
```bash
nohup mutatex BTKPRK.pdb -p 4 -m mutation_list.txt -x /home/ctools/foldx/foldx -f suite5 -R repair_runfile_template.txt -M mutate_runfile_template.txt -q poslist.txt -L -l -v -C  none -B  -I interface_runfile_template.txt &
```

6. extract the data to csv file
for 6YYG-WASP
```bash
ddg2excel -p 6YYG_WASP.pdb -l mutation_list.txt -q poslist.txt -d results/interface_ddgs/final_averages/A/ -F csv
```

and 5P9I-PRKCQ
```bash
ddg2excel -p BTKPRK.pdb -l mutation_list.txt -q poslist.txt -d results/interface_ddgs/final_averages/A/ -F csv
```

7. Create the heatmap based on the data
for 6YYG-WASP
```bash
ddg2heatmap -p 6YYG_WASP.pdb -l mutation_list.txt -q poslist.txt -d results/interface_ddgs/final_averages/A/
```
for 5P9I-PRKCQ
```bash
ddg2heatmap -p BTKPRK.pdb -l mutation_list.txt -q poslist.txt -d results/interface_ddgs/final_averages/A/
```

