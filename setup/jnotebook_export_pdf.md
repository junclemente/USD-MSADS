
# Exporting Jupyter Notebook to PDF

To export your notebook to PDF, you will need to install a few more libraries.

Open your conda environment: `conda activate <environment name>`

To be consistent, I install everything from the conda-forge repository, hence
the use of `-c conda-forge`.

## Install nbconvert

Install `nbconvert`:

```
conda install -c conda-forge nbconvert
```

## Install pandoc

Install `Pandoc`

```
sudo apt-get install pandoc
```

## Install TeX

Install `TeX`
This is a large download so it may take some time to install.

```
sudo apt-get install texlive-xetex texlive-fonts-recommended texlive-plain-generic
```

**Source:** [Installing Nbconvert](https://nbconvert.readthedocs.io/en/latest/install.html#supported-python-versions)
