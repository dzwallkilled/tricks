# Conda
Conda installation: https://docs.anaconda.com/anaconda/install/linux/

After installation, create a new virtual environment
  
>$conda create -n myenv python=3.6

More details please refer to https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-with-commands

Activate the environment just created 
>$conda activate myenv

The console will show like the following
>(myenv)$

Note: each time connecting to the server via ssh, the console will actiate the environment by default. If you have multiple conda environments, please activate specific environment you wanna use. Or you can set the automatic conda activation to false.

Install packages in that environment
>(myenv)$conda install numpy matlibplot scipy 

Anaconda cheatsheet: https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf


# Pytorch
Install via conda (firstly, you need to activate the corresponding conda environment)
>(myenv)$conda install pytorch torchvision torchaudio cudatoolkit=11.0 -c pytorch

Note: the current cuda version on our server (amrl-hpcgx) is 11.0


# Pycharm
Installation: 
  1. Download https://www.jetbrains.com/pycharm/download/#section=mac
  2. Or install [jetbrain toolbox](https://www.jetbrains.com/toolbox-app/) and install/manage pycharm via toolbox
  

  
# Some tricks
To install packages, we need to connect the server to the internet.  
>$bash border.sh open  
>$(your usrname, e.g. zd027)  
>$(your password) 
>$Autheration success!  
  
## CUDA commands
Check the availability of GPU devices
>$nvidia-smi  
or  
>$watch -n.5 nvidia-smi

Note: the second command tells the console to run `nvidia-smi` every 0.5 second, i.e. refreshing the GPU status in real-time. Press `Ctrl+C` to stop.
