__The Place__

What is a caveman? A prominent announced trend in usage and development in the Jupyter ecosphere is toward Jupyterlab, undoubtedly a strong and popular product. Nevertheless, some 'paleo', even 'neanderthal', individuals stick stubbornly to the classic notebook. Similar to a caveman role. That's me, Mr. Neanderthal.
   
The purpose of this repository is twofold: One, to show how to set up a purely classical notebook environment, and Two, to show how to run the demo problem from __vmc_pde__  to appreciate an interesting, even an important, approach to partial differential equation solving.

__The Distro__

Why use Mint 20.2 ? For some reason, Python 3.10 throws a spurious runtime error on the sample problem. Python 3.9 is fine, but as a policy decision, Mint restricts the installed Python sub-versions to even numbers. This makes 20.2 the natural choice, since it ships with Python 3.8.10, the highest version available in Mint which is less than 3.10.

__Download It__

Download Mint 20.2 XFCE version. The downloaded iso is about 1.9 GB in size.

__Etch It__

Balena Etcher writes the iso to a bootable executable on a SD chip.

<img src="https://github.com/whiffee/Jupyter_caveman/blob/main/balena.png" width=40% height=40%/>

__Install It__

The iso can be installed as either a virtual machine _a la_ Virtual Box, or as an independent drive. I made three test runs with a standalone SSD to validate the procedure outlined here.

__Run It__

Once the distro is running, you can add some preferred applications if desired, such as Mousepad, PCManFM, or Synaptic. When the basic articles are in place, download the code from the caveman repository and unzip it in the Downloads directory.

__Install the Python Framework__

Right click the unzipped caveman directory and open it in a terminal. You can type _ls_ to view the directory contents. Then run the installation command. It's actually pretty neat that pip can install any number of modules named in a text list, meanwhile ensuring that the exact version you specify is installed in each case. 

<img src="https://github.com/whiffee/Jupyter_caveman/blob/main/install_requirements.png" width=70% height=70%/>

__Make a Freeze List__

After the installations are complete, you can do a sanity check on the freeze list. Notice that there are no lines in the list for Jupyterlab or Jupyterlab_server.

<img src="https://github.com/whiffee/Jupyter_caveman/blob/main/pip-freeze.png" width=30% height=30%/>

__Install jaxlib__

The vmc_pde instruction notes specify to use jaxlib version 1.7.4. However, (not that it matters) I found that version 1.75 is also usable. Notice that within numerical version siblings, pip will choose the file which matches Python 3.8.

<img src="https://github.com/whiffee/Jupyter_caveman/blob/main/install_jaxlib174.png" width=80% height=80%/> 

__Install mpi4py__

If the module mpi4py is included in the requirements.txt list, it will install smoothly initially, but get kicked out later, before the end, and in such a way that it can't be re-installed directly. I took a hint from Stack Overflow question 28440834, first installing the dev version of Open MPI, and then installing mpi4py without specifying the desired version. (It installed version 4.0.3 on 11 May 2025).

<img src="https://github.com/whiffee/Jupyter_caveman/blob/main/install_openmpi_dev.png" width=73% height=73%/>

<img src="https://github.com/whiffee/Jupyter_caveman/blob/main/install_mpi4py.png" width=73% height=73%/>

__Download the VMC_PDE Code__

Download the __vmc_pde__ sample problem code and extract it into a directory.

__Install the Python IDE PYZO__

To get a quick look at the viability of the code execution machinery, install the Pyzo program.

<img src="https://github.com/whiffee/Jupyter_caveman/blob/main/install_pyzo.png" width=73% height=73%/>

__Test the Sample Code__

Directly test the sample problem using Pyzo. Open the main.py module, located within the Fluids directory, and run it as a script. The data, tables, and all 19 figures should be generated. The figures are initially rendered as bare frames, then filled in at the end. Having demonstrated that the code is viable, you can move on to testing the functionality of the Jupyter version.

__Edit the PATH__

In the home directory there is a file called .bashrc. It is necessary to edit this file to get permanent effective change in the $PATH. The permanent change that is desired is access to some designated import directory, which can hold the modules that the application will need to import as ancillaries. At the very end of the file place a $PATH change statement similar to the one shown on the last line of the image below.

<img src="https://github.com/whiffee/Jupyter_caveman/blob/main/bashrc_snippet.png" width=61% height=61%/>

__Test Jupyter Rendition__

Right click on the target directory that was the subject of the $PATH statement in the .bashrc file, open a terminal, and start Jupyter notebook from there. Open a notebook file such as the one included from the caveman repository, and execute the cell containing the __vmc_pde__ test problem. All the output for the sample problem that was shown in Pyzo should become available.


  
