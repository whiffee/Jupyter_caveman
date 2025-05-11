__The Place__
$\hspace{1.5 em}$What is a caveman? A prominent Jupyter trend in usage and development is toward Jupyterlab. But some paleo, even neanderthal, individuals stick stubbornly to the classic notebook. Almost like a caveman. That's me, Mr. Neanderthal.
$\hspace{1.5 em}$The purpose of this repository is twofold: One, to show how to set up a purely classical notebook environment, and Two, to show how to run the demo problem from vmc_pde  for an interesting, even important, approach to partial differential equation solving.

__The Distro__
$\hspace{1.5 em}$Why Mint 20.2? Python 3.10 throws a spurious runtime error on the sample problem. Python 3.9 is fine, but Mint restricts the installed Python sub-versions to even numbers. Hence 20.2, which ships with Python 3.8.10.

__Download It__
$\hspace{1.5 em}$Download Mint 20.2 XFCE version. The downloaded iso is about 1.9 GB in size.

__Etch It__
$\hspace{1.5 em}$Balena Etcher writes the iso to a bootable executable on a SD chip.

__Install It__
$\hspace{1.5 em}$The iso can be installed as either a virtual machine _a la_ Virtual Box, or as an independent drive. I made three test runs with a standalone SSD to test the procedure outlined here.

__Run It__
$\hspace{1.5 em}$Once running, you can add personal prefs if desired, such as Mousepad, PCManFM, and Synaptic. Then download the code from the caveman repository and unzip it in the Downloads directory.

__Install the Python Framework__
$\hspace{1.5 em}$Right click the unzipped directory and open it in a terminal. Then run

__Make a Freeze List__


$\hspace{1.5 em}$You can do a sanity check on the freeze list. Notice that there are no lines for Jupyterlab or Jupyterlab_server.


https://github.com/whiffee/Jupyter_caveman/blob/main/pip-freeze.png

__Install jaxlib__
$\hspace{1.5 em}$The vmc_pde instruction notes specify jaxlib version 1.7.4. However, (not that it matters) I found that version 1.75 is also usable. Notice that pip will choose the file which matches Python 3.8.

__Install chex__
$\hspace{1.5 em}$If installed with the other framework imports, chex may cause turbulence, so it is installed by itself at this point.

__Install mpi4py__
$\hspace{1.5 em}$Installing mpi can be a little tricky. A workable method I found was to first install openmpi, then to install mpi4py right on top of it.

__Download the VMC_PDE Code__
$\hspace{1.5 em}$Download the vmc_pde sample problem code and extract it to a directory.

__Test the Sample Code__
$\hspace{1.5 em}$Direct testing of the sample problem using Pyzo. Open the main.py module and run it as a script. The data, tables, and all 29 figures should be generated. The figures are initially rendered as bare frames, then filled in at the end.

__Edit the PATH__
$\hspace{1.5 em}$After editing the path to provide access to an import directory, the Jupyter functionality will be ready to test. There is no need to bother with _jupyter\_notebook\_config.py_.

__Test Jupyter Rendition__
$\hspace{1.5 em}$Open Jupyter and test a notebook file such as the one included from the caveman repository. All the output for the sample problem that was shown in Pyzo should become available.


  
