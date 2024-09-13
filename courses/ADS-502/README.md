# Creating a Python and R environment in WSL2

In this class, it is necessary to code in both Python and R.
I prefer using Jupyter Notebooks in VSCode over RStudio, even though it was
much easier to setup RStudio to run both languages.

Unfortunately, [rpy2](https://rpy2.github.io/doc/latest/html/introduction.html)
is required to use Python and R in Jupyter Notebooks but
there are no binaries for rpy2 that work in Windows as of the
writing of this post (July 2024).

Therefore, the work around is to create the environment in WSL2 and use
VSCode extensions to remote into the WSL2 environment.

## Install Windows Subsystem for Linus (WSL2)

If you do not already have WSL2 installed on your Windows machine, follow the
directions on this page to install WSL2 and Ubuntu.

Open powershell and type the following:

```powershell
wsl --install

```

This will install WSL2 and Ubuntu by default.

**Source:** [How to install Linux on Windows WSL](https://learn.microsoft.com/en-us/windows/wsl/install)

## Install miniconda in Ubuntu (WSL2)

Next, open Ubuntu and install miniconda.

Enter the following lines:

```
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
```

After installing miniconda, initialize the bash and zsh shells:

```
~/miniconda3/bin/conda init bash
~/miniconda3/bin/conda init zsh
```

**Source:** [Miniconda: Quick command line install](https://docs.anaconda.com/miniconda/)

## Create a conda environment with Python and R

Type the following to create the conda environment. This will create an
environment named "cobRa". You can replace this with any name you want.
This will also install python version 3.10.12. If you would like to install a
different version, replace the version number, or, remove 'python=3.10.12'
completely to install the latest version of python.

```
conda create -c conda-forge -n cobRa python=3.10.12 ipython rpy2 r r-essentials pandas numpy seaborn matplotlib scikit-learn jupyter statsmodels pydotplus
```

### Renaming the conda environment

Just thinking of some fun environment names: vipeR, seRpent, Rython, rattleR, scaleR

If you decide that you want to change the name of your environment you can
use `conda rename` by typing the following:

```
conda rename -n <name of old env> <name of new env>
```

## Running Jupyter Notebook from WSL2

You can activate the conda environment with the following:

```
conda activate <environment name>
```

### Start jupyter notebook

And you should be able to start Jupyter Notebooks once you're in the
environment by typing:

```
jupyter notebook
```

### Open the notebook in the browser

This will start the Jupyter Notebook server but it may not open up a browser
window. To view the notebook, follow the instructions in the console to get
the address of the notebook. It should look like this:

```
To access the server, open this file in a browser:
   file:///home/jc/.local/share/jupyter/runtime/jpserver-310846-open.html
Or copy and paste one of these URLs:
   http://localhost:8888/tree?token=c8c48b06310ff4f4b31bc3c5328c0cd4fd9421d7941d475b
   http://127.0.0.1:8888/tree?token=c8c48b06310ff4f4b31bc3c5328c0cd4fd9421d7941d475b
```

**Note:** The token will be different every time you restart the server.

## WSL2 extension for Visual Studio Code (VSCode)

If you don't have VSCode installed, download from here: [Visual Studio Code](https://code.visualstudio.com/)

### Install WSL Extension

Install the WSL Extension to allow VSCode to connect to WSL by installing the
extension and following the instructions on this page:

[Remote development in WSL](https://code.visualstudio.com/docs/remote/wsl-tutorial)

### Launch VS Code from WSL

To begin programming in VSCode using the WSL environment:

1. Open the WSL terminal.
2. Activate your environment: `conda activate <environment name>`.
3. Switch to the directory of your project: `cd \path\to\project`.
4. Open VSCode by typing: `code .`.

This will open up VS Code in your project directory and connected to WSL.

**Source**: [WSL Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl#:~:text=The%20WSL%20extension%20lets%20you,as%20you%20would%20from%20Windows.)

## Exporting Jupyter Notebook to PDF

To export your notebook to PDF, you will need to install a few more libraries.

Open your conda environment: `conda activate <environment name>`

To be consistent, I install everything from the conda-forge repository, hence
the use of `-c conda-forge`.

### Install nbconvert

Install `nbconvert`:

```
conda install -c conda-forge nbconvert
```

### Install pandoc

Install `Pandoc`

```
sudo apt-get install pandoc
```

### Install TeX

Install `TeX`
This is a large download so it may take some time to install.

```
sudo apt-get install texlive-xetex texlive-fonts-recommended texlive-plain-generic
```

**Source:** [Installing Nbconvert](https://nbconvert.readthedocs.io/en/latest/install.html#supported-python-versions)

## Creating a conda environment from a yml file.

```
conda env create -n ENVNAME --file ENV.yml
```

## Creating a conda environment from a yml file.

```
conda create -n ENVNAME --file ENV.txt
```

## Aliases in WSL2 (Ubuntu)

To make things easier to start coding, I created an alias, like `ads502`, that
goes to my ADS502 folder, activates my `vipeR` environment and then opens
VSCode.

To create your own aliases,

1. Create a file called `.bash_aliases` if it doesn't exist yet.
2. Open the file in a text editor such as nano.
3. Create an alias such as: `alias ads502="cd ~/msads-code/ADS502 && conda activate vipeR && code ."`
4. Load the aliases file by typing: `source ~/.bashrc`.
5. Start by typing your alias...
6. If everything was done right, your terminal window should show that you are in the correct directory and that VS Code is starting up.

## Forgot WSL2 sudo password

Oops... you forgot your password?

In a terminal outside of WSL:

1. Run `wsl -u root`
2. Run `passwd <username>`
3. Enter new password.

**Source:** [How to reset my WSL Ubuntu password?](https://github.com/junclemente/MSADS-MISC/tree/main/502)
