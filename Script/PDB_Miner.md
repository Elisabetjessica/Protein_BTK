This script run PDB Miner for Burton's Tyrosine Kinase (BTK) protein, with Uniprot Accession Code (UPAC): Q06187, structure selection.

Step 1: Initialise conda environment for the first time
```bash
> /home/ctools/anaconda3-2024.10-1/bin/conda init
```
Step 2: disconnect from the server and reconnect 

Step 3: activate the conda environment 
> conda activate /home/ctools/protein_structure_course

Step 4: run the PDBminer software
> nohup PDBminer -u Q06187 -n 2 -f csv &

Additional script for interactor protein, Protein kinase C theta type (PRKCQ) with Uniprot Accession code (UPAC): Q04759, structure selection.

Step 1: activate the conda environment 
> conda activate /home/ctools/protein_structure_course

Step 2: run the PDBminer software
> nohup PDBminer -u Q04759 -n 2 -f csv &
