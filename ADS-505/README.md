# ADS505 - Applied Data Science for Business

## Creating a conda environment from a yml file

To create an environment with a specific name:

```
conda env create -n ENVNAME -f ENVNAME.yml
```

To create an environment using the name in the YAML file:

```
conda env create -f ENVNAME.yml
```

Update environment:

```
conda env update -f local.yml --prune
```
