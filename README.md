# Protein_BTK
This repository contains the workflow and code used in the structural analysis of Burton's Tyrosine Kinase (BTK) utilizing MAVISp framework. The workflow integrates **PDB miner** for structure selection, **MutateX** for calculating local interaction and binding free energy, and **CABS-flex** for molecular dynamics simulations to assess structural flexibility. 

## Project Workflow
This project workflow is as follow
1. Protein structure curation and selection with PDBminer
2. Solvent accessibility analysis with Naccess and folding free energy calculation with MutateX
3. Binding free energy calculation with MutateX
4. Molecular Dynamic simulation with CABS flex 2.0
5. Folding free energy calculation with MutateX Ensemble mode
   
# Reference
```bash
PDBminer to Find and Annotate Protein Structures for Computational Analysis
Kristine Degn, Ludovica Beltrame, Matteo Tiberti, Elena Papaleo
Journal of Chemical Information and Modeling, 2023, doi: 10.1021/acs.jcim.3c00884
```

```bash
MutateX: an automated pipeline for in-silico saturation mutagenesis of protein structures and structural ensembles Matteo Tiberti*, Thilde Terkelsen, Kristine Degn, Ludovica Beltrame, Tycho Canter Cremers, Isabelle da Piedade, Miriam Di Marco, Emiliano Maiani, Elena Papaleo*, Brief Bioinform. 2022 Mar 22;bbac074. doi: 10.1093/bib/bbac074
```

```bash
MAVISp: Multi-layered Assessment of VarIants by Structure for proteins
Matteo Arnaudi, Ludovica Beltrame, Kristine Degn, Mattia Utichi, Pablo Sánchez-Izquierdo, Simone Scrima, Francesca Maselli, Karolina Krzesińska, Terézia Dorčaková, Jordan Safer, Katrine Meldgård, Julie Bruun Brockhoff, Amalie Drud Nielsen, Alberto Pettenella, Jérémy Vinhas, Peter Wad Sackett, Claudia Cava, Sumaiya Iqbal, View ORCID ProfileMatteo Lambrughi, Matteo Tiberti, Elena Papaleo biorxiv, doi: https://doi.org/10.1101/2022.10.22.513328
```
```bash
CABS-flex 2.0: a web server for fast simulations of flexibility of protein structures
Aleksander Kuriata , Aleksandra Maria Gierut , Tymoteusz Oleniecki , Maciej Paweł Ciemny , Andrzej Kolinski , Mateusz Kurcinski , Sebastian Kmiecik
https://doi.org/10.1093/nar/gky356
```
