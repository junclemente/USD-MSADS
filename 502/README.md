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

## Install WSL2

If you do not already have WSL2 installed on your Windows machine, follow the
directions on this page to install WSL2 and Ubuntu.

Open powershell and type the following:

```powershell
wsl --install

```

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

**Source:** [Quick command line install](https://docs.anaconda.com/miniconda/)

## Create a conda environment with Python and R
