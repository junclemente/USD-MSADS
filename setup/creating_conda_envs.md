# Creating a Conda environment from a yml file

To create an environment with a specific name:

```bash
conda env create -n ENVNAME -f <path_to_ENVNAME.yml>
```

To create an environment using the name in the YAML file:

```bash
conda env create -f ENVNAME.yml
```

Updating the environment:

```bash
conda env update -f <path_to_ENVNAME.yml> --prune
```
