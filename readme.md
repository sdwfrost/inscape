# INSCAPE 
HCV directionality prediction software implemented in python  
Based off Pavel Skums' [QUENTIN](https://github.com/skumsp/quentin)
Call this program on a suspected cluster of clinical samples of viral dna for transmission network inference  
Python 2.7 code
# Prerequisites
### python modules which are not in the standard library
numpy  
scipy  
fastcluster  
six  
biopython  
networkx  
cvxopt  
### other prerequisites
[lsqlin.py](https://github.com/scivision/airtools/blob/master/airtools/lsqlin.py) (included on this github)
[graphviz](http://www.graphviz.org/)
[mafft](http://mafft.cbrc.jp/alignment/software/)

# Usage Information

This is a scientific command line style script, so all you have to do to install is clone this repository and perform the above prerequisite installations
If you have any questions, you can reach me at Joseph.Gussler@cdc.hhs.gov

# A note about input formatting
Input must be a valid FASTA file.

This program expects viral quasispecies populations (a pool of closely related mutants achieved through deep amplicon sequencing)

For each entry, your sequence ID should end with a number following the trailing underscore which denotes the frequency of that variant. For example, here we have a sequence ID with a bunch of extra information that will give the appropriate frequency of 25 for that variant

```
>P06_run12_alaska_3_2_25
```
# What else is in this repository?

EvolutionSimulation.gif - a looping short video which illustrates the process by which we simulate evolution from one patient to another

spreader.fas, target.fas - two very small FASTA files which could be used to test your installation

exampleout.png - expected output from running the following command:
```
python inscape.py spreader.fas target.fas
```
This command will run the program assuming lsqlin.py, inscape.py and the hcv fasta files are all in the current working directory. Your output (default tmp.png) should look similar to exampleout.png

For help with other options, simply type  
```
python inscape.py -h
```
LICENSE.txt - GNU public license
    
# Acknowledgements
Valeriy Vishnevskiy - lsqlin.py
Pavel Skums - came up with the algorithm for QUENTIN  
The rest of the DVH bioinformatics team @ CDC  
