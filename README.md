# Adversarial-Domain-Adaptation-for-Identifying-Phase-Transitions
Python code for our paper "Adversarial Domain Adaptation for Identifying Phase Transitions"

## How to use this code:

To train the DANN there are changes that have to be done in the keras source files.
We recommend to make a new environment for this.
If the DANN is trained and you want to test it, we recommend to deactivate this new
environment, because some times there is a bug appearing and the predictions of the 
NN are wrong. This still has to be fixed.


## INSTALL

- create new environment: conda create -n dann anaconda

- activate the environment: source activate dann

- replace 'training.py' in /home/USERNAME/.conda/pkgs/keras-2.0.5-py36_0/lib/python3.6/site-packages/keras/engine
by the 'training.py' file in the folder. 
'training_old.py' is the original file. Keep it, just in case.
If the path cannot be found start python and type:
	import keras as ker
	ker.__file__


## Files

### GUTZWILLER

- Code partially from https://github.com/tcompa/BoseHubbardGutzwiller, install these files to use our code.
- With this file we generated the Gutzwiller coefficients.


### Gradient Reverse Layer
- Code from https://github.com/fchollet/keras/issues/3119#issuecomment-230289301
- Has to be in the same folder as the python script with the DANN code.

### DANN_helper_file


### DANN Implementation
https://github.com/fchollet/keras/pull/4031/files

### Bogoliubov_Kitaev
Produces Kitaev states

### SSH_states_and_Winding_Nr
Produces SSH states for OBC and PBC and calculates
also the winding number and gives a plot of it.

To do the same for long range SSH, replace the
Hamiltonian in this file with the Hamiltonian from
SSH_Long_Range_Hamiltonian.py

### Ising