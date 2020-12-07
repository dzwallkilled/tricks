# Conda
Conda installation: https://docs.anaconda.com/anaconda/install/linux/

After installation, create a new virtual environment
  
>$conda create -n myenv python=3.6

More details please refer to https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-with-commands

Activate the environment just created 
>$conda activate myenv

The console will show like the following
>(myenv)$

Install packages in that environment
>$conda install numpy matlibplot scipy 

Anaconda cheatsheet: https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf


# Pytorch
Install via conda (first activate the corresponding conda environment)
>$conda install pytorch torchvision torchaudio cudatoolkit=11.0 -c pytorch

Note: the current cuda version on our server (amrl-hpcgx) is 11.0



# Pycharm
Installation: 
  1. Download https://www.jetbrains.com/pycharm/download/#section=mac
  2. Or install [jetbrain toolbox](https://www.jetbrains.com/toolbox-app/) and install/manage pycharm via toolbox
