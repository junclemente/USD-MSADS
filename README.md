# Masters of Science in Applied Data Science
## University of San Diego

This repository is where I have files and references that I can share for 
anyone who finds it useful. 

For the most part, these are some of the notes that I refer to on a regular 
basis. 

### Custom functions

These are a few functions I wrote to help with some of the coding that we
have to do repeatedly.

The functions from this notebook can be imported into another notebook by
using the `%run` command in a code cell:

```
%run <path to notebook>
```

This will make the functions useable in the notebook.

### Environments Creating a conda environment from a yml file

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