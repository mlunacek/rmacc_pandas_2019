Contents
========


- Install `git`
- Install Python
- Set up training environment. 

# Install `git`

* Windows
    * Download latest verison of `git` (2.21.0) from <https://git-scm.com/downloads>
    * Ensure `Git Bash Here` is selected (default)
    * Ensure `Git GUI Here` is selected (default)
    * Select `Use Git from the Windows Command Prompt` (default)
    * Select `Checkout Windows-style, commit Unix-style line endings` (default)
    * Select `Use MinTTY (the default terminal of MSYS2)` (default)
    * Hit Next for remaining
* OSX
    * If you have `git` on your machine, you can skip this step. 
    * Download latest version of `git` (2.21.0) from <https://git-scm.com/downloads>
    * If using git for the first time from terminal, you may get a prompt to say GIT not installed do you want to download? Select yes (you don’t need the full Xcode)


# Install Python 3

**Using Anaconda**

_Note: If you already have Anaconda2 or Anaconda3 run `conda update anaconda` and then `conda update conda` from the command line._

_Note: This training relies on Python 3 features. If you have Anaconda2, you can install Python 3 in a conda environment. For more information on how to set up an environment, see the next section_


1. Download the latest version of Anaconda3 x64 from Continuum <https://www.continuum.io/downloads>. You don't have to enter any contact information if you don't want to.
    * Windows
        * Click on Anaconda3-4.3.1-Windows-x86_64.exe and follow instructions

    * OSX
        * Click on Anaconda3-4.3.1-MacOSX-x86_64.dmg and follow instructions

2. Verify that conda has been installed
    * Try `which conda` and make sure you see anaconda in the return value. Or
    * `conda --version` should result in `conda 4.3.1`  
  
Do not proceed if you do not see `anaconda` in the path when you type `pip --version`. If you do not see anaconda, reinstall anaconda and check if the installation was successful. If you still do not see anaconda in the path, check your `$PATH` variable to see if the directory to anaconda exists.

You will have to open a new shell to ensure that conda is in your environment.

# Set up training environment

* Windows
   * Open `Git Bash` and type the following

```
cd C:
mkdir GitRepos
cd GitRepos
git clone https://github.com/mlunacek/rmacc_pandas_2019.git
cd rmacc_pandas_2019
```

* Mac
   * Open `Terminal` and type the following

```
cd ~
mkdir GitRepos
cd GitRepos
git clone https://github.com/mlunacek/rmacc_pandas_2019.git
cd rmacc_pandas_2019
```

### Conda Environment

The easiest way to get everything you need is to type:

```
conda env create -f environment.yml
```

_Note_

If you are having issues with conda the network

```
conda config --set ssl_verify false
```

We recommend using conda for installing packages. If you are unable to find a package in conda, then try `pip install package_name`

_Conda environment with all packages required for the training_

```
conda env create -f environment.yml
source activate python_training
```

If you want to exit the environment, you can run `source deactivate`. 


### Additional notes

Most machines come with Python pre-installed. Newer versions of Python may already have pip, and you may have used it in the past to install packages. Installing a fresh version Anaconda should add a new version of Python and pip in a separate location. On uninstalling Anaconda or if you change your `$PATH` variable, you can access your old version of Python and pip, and all the packages you installed previously.

# Credits

Prepared at NREL by:

* Dheepak Krishnamurthy
* Bryan Palminitier
* Monte Lunacek
