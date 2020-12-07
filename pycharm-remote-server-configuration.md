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
  
## Project Interpreter
GO to preference  
<img src="https://github.com/dzwallkilled/tricks/blob/master/remote_debug_imgs/preferences.jpg" width="600" />
  
Select the project interpreter, and select add:  
<img src="https://github.com/dzwallkilled/tricks/blob/master/remote_debug_imgs/project_interpreter.jpg" width="600" />


Select adding SSH interpreter, and input the server IP address and password,  
<img src="https://github.com/dzwallkilled/tricks/blob/master/remote_debug_imgs/add1.jpg" width="600" />

If account and password are valid, select the python execute file (bin file), e.g. the bin file in conda environment.  
<img src="https://github.com/dzwallkilled/tricks/blob/master/remote_debug_imgs/add2.jpg" width="600" />

Note: you can add as many remote (SSH) interpreters as you want, e.g. adding an interpreter for each environment on remote sever for PyTorch/TensorFlow/projects etc.

## Deployment
After interpreter configuration, you can debug on remote server. However, one issuse is that you might need to upload all the codes each time. Hence, it is better to have a backup of your codes on remote server. The codes will be synchronized everytime local changes occour. Also, after deployment configuration, you can view remote contents, including folders and files.


Select tools/deployment/configuration  
<img src="https://github.com/dzwallkilled/tricks/blob/master/remote_debug_imgs/deployment.jpg" width="600" />

Fillin the details in connection. In mappings, select the path to store the codes on remote server. __Note that this is project specific__.
<img src="https://github.com/dzwallkilled/tricks/blob/master/remote_debug_imgs/mappings.jpg" width="600" />

Another advantage of the deployment is users can start console easily by selecting tools/start SSH session. By logining remote console, users can run bash commands easily, e.g. `$nvidia-smi`.


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
