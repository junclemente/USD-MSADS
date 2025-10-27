# Creating a Python and R environment in WSL2

Some of the classes for the MS-ADS course require programming in both Python and R. I prefer using Jupyter Notebooks in VSCode over RStudio, even though it was much easier to setup RStudio to run both languages.

Unfortunately, [rpy2](https://rpy2.github.io/doc/latest/html/introduction.html) is required to use Python and R in Jupyter Notebooks but there are no binaries for rpy2 that work in Windows as of the writing of this post (July 2024).

Therefore, the work around is to create the environment in WSL2 and use VSCode extensions to connect remotely into the WSL2 environment.


# Create a Conda environment with Python and R

## Using the included YAML file

You can use the `environments\cobRa.yml` file or create your own YAML file. This file contains the minimum required libraries necessary to run both Python and R in the same environment. 

Use the following command to create the `cobRa` environment from the provided YAML file:

```bash
conda env create -f /path/to/environment/cobRa.yml
``` 
This will create the environment with Python 3.10 and other required libraries: 
- ipython
- rpy2
- r
- r-essentials
- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn
- jupyter
- statsmodels
- pydotplus
- pip

## Using the CLI
Instead of using the YAML file, the environment can also be created without using the YAML file:

```bash
conda create -c conda-forge -n cobRa python=3.10.12 ipython rpy2 r r-essentials pandas numpy seaborn matplotlib scikit-learn jupyter statsmodels pydotplus
```

# Running Jupyter Notebook from WSL2

You can activate the conda environment with the following:

```bash
conda activate <environment name>
```

## Start jupyter notebook

And you should be able to start Jupyter Notebooks once you're in the
environment by typing:

```bash
jupyter notebook
```

## Open the notebook in the browser

This will start the Jupyter Notebook server but it may not open up a browser
window. To view the notebook, follow the instructions in the console to get
the address of the notebook. It should look like this:

```bash
To access the server, open this file in a browser:
   file:///home/jc/.local/share/jupyter/runtime/jpserver-310846-open.html
Or copy and paste one of these URLs:
   http://localhost:8888/tree?token=c8c48b06310ff4f4b31bc3c5328c0cd4fd9421d7941d475b
   http://127.0.0.1:8888/tree?token=c8c48b06310ff4f4b31bc3c5328c0cd4fd9421d7941d475b
```

**Note:** The token will be different every time you restart the server.

# WSL2 extension for Visual Studio Code (VSCode)

If you don't have VSCode installed, download from here: [Visual Studio Code](https://code.visualstudio.com/)

## Install WSL Extension

Install the WSL Extension to allow VSCode to connect to WSL by installing the
extension and following the instructions on this page:

[Remote development in WSL](https://code.visualstudio.com/docs/remote/wsl-tutorial)

## Launch VS Code from WSL

To begin programming in VSCode using the WSL environment:

1. Open the WSL terminal.
2. Activate your environment: `conda activate <environment name>`.
3. Switch to the directory of your project: `cd \path\to\project`.
4. Open VSCode by typing: `code .`.

This will open up VS Code in your project directory and connected to WSL.

**Source**: [WSL Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl#:~:text=The%20WSL%20extension%20lets%20you,as%20you%20would%20from%20Windows.)
