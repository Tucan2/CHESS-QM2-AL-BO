## Create a python environment at lnx201

#### ✅ Step 3: Login to the lnx201
`ssh -Y <username>@lnx201.classe.cornell.edu`

#### ✅ Step 2: Start an Interactive Job Session
  - Once logged in, run:
        `qrsh -q interactive.q -l mem_free=200G -pe sge_pe 8` 

#### ✅ Step 3: Go to the fife location
        `cd /nfs/chess/sw` 

#### ✅ Step 4: Go to the life location
        `python3 -m venv <name of your python env>` 
Example: 
        `python3 -m venv qm2_BO`

#### ✅ Step 5: activate environment
        `source /nfs/chess/sw/<name of your python env>/bin/activate` 
Example: 
        `source /nfs/chess/sw/qm2_BO/bin/activate` 

you can install your own python environments and have them added as an option when creating new notebooks.

Create your own python environment using your desired python installation. Please see LinuxSoftwareDevelopment for a list of centrally maintained python environments, and further down LinuxSoftwareDevelopment for tips on creating your own conda installation.

Install anything you like in the environment, but you MUST at least install ipykernel. For example

pip install ipykernel

Activate the new environment. If using conda, this would look something like:

source /path/to/conda/install/bin/activate conda activate my-python-env

Add the virtual environment as a jupyter kernel using

python -m ipykernel install --user --name=my-python-env --display-name "My Python Env"

This adds the kernel to ~/.local/share/jupyter/kernels/ and now it can be used by Jupyter. When you create a new notebook now, “My Python Env” will be one of your choices.

