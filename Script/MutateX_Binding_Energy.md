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
 
