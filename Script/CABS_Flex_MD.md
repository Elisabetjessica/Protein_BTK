This script run for Molecular Dynamics simulation with CABS-flex 2.0

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
nohup CABSflex -i 5P9I_No.pdb -k 10 -y 30 -a 10 -v 3 -z 10 -A --log &
```
for 6YYG structure
```bash
nohup CABSflex -i 6YYG_A_clean.pdb -k 10 -y 30 -a 10 -v 3 -z 10 -A --log &
```


