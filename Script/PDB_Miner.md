this script run PDB Miner for Burton's Tyrosine Kinase (BTK) protein with Uniprot Accession Code (UPAC): Q06187

Step 1: Initialise conda environment for the first time
/home/ctools/anaconda3-2024.10-1/bin/conda init

Step 2: disconnect from the server and reconnect 

Step 3: activate the conda environment 
conda activate /home/ctools/protein_structure_course

Step 4: nohup PDBminer -u UPAC -n 2 -f csv &
