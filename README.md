This repository contains the source codes for the paper, '**Conditional TMDTO as a MILP Instance**'. 


## Description of the Attack
In this paper, we have converted the conditional Time-Memory-Data Tradeoffs problem to a set of linear constrainst and objective functions for the case of stream cipher. Briefly, the problem can be stated as follows:

*What is the minimum number of state bits should be fixed in order to recover a maximum number of state variables directly from the keystream bits while guessing rest of the state bits ?* 

We have addressed this problem for the case where we are allowed to fix the state bits to 0 only. This repository contains the code to convert the above problem to an instance of Mixed Integer Linear Programming (MILP). We have implemented it on three stream ciphers: ```Lizard```, ```Grain-128a``` and ```Espresso```.
## File Structure

1. ```Espresso/```: This folder contains the scripts for TMDTO attack on ```Espresso``` cipher.
2. ```Grain-128a/```: This folder contains the MILP scripts for TMDTO attack on ```Grain-128a``` cipher.
3. ```Lizard/```: This folder contains the MILP scripts for TMDTO attack on ```Lizard``` cipher.
## Dependencies

* [Gurobi](https://www.gurobi.com/)
* [Python3](https://www.python.org/download/releases/3.0/)
## Install and Setup Gurobi

1. Create a virtual environment with conda: ```conda create -n TMDTO_MILP```
2. Activate the new environment: ```conda activate TMDTO_MILP```
3. Add Gurobi channels as follows: ```conda config --add channels https://conda.anaconda.org/gurobi```
4. Install Gurobi using conda: ```conda install gurobi``` (academic users can obtain this license)
5. Activate license using the command: ```grbgetkey <license-number>```
