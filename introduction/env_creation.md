# Create a python environment at lnx201







you can install your own python environments and have them added as an option when creating new notebooks.

Create your own python environment using your desired python installation. Please see LinuxSoftwareDevelopment for a list of centrally maintained python environments, and further down LinuxSoftwareDevelopment for tips on creating your own conda installation.

Install anything you like in the environment, but you MUST at least install ipykernel. For example

pip install ipykernel

Activate the new environment. If using conda, this would look something like:

source /path/to/conda/install/bin/activate conda activate my-python-env

Add the virtual environment as a jupyter kernel using

python -m ipykernel install --user --name=my-python-env --display-name "My Python Env"

This adds the kernel to ~/.local/share/jupyter/kernels/ and now it can be used by Jupyter. When you create a new notebook now, “My Python Env” will be one of your choices.

