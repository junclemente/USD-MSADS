# 🧩 Creating and Updating Conda Environments from a YAML File

Conda environment YAML files make it easy to share, recreate, or update environments with the same dependencies across systems.


---

## 🆕 Create a New Environment

Create an environment **with a custom name** (overrides the name in the YAML file):

```bash
conda env create -n <ENVNAME> -f <path_to_ENVNAME.yml>
```

Or create the environment **using the name defined inside the YAML file**:

```bash
conda env create -f <path_to_ENVNAME.yml>
```

---

## 🔄 Update an Existing Environment

To update all dependencies to match the YAML file (and remove anything not listed):

```bash
conda env update -f <path_to_ENVNAME.yml> --prune
```

> 💡 The `--prune` flag ensures obsolete packages are removed, keeping the environment clean.

---

## 🧹 Optional Maintenance

List all environments:

```bash
conda env list
```

Remove an environment:

```bash
conda env remove -n <ENVNAME>
```

Export the current environment to a new file:

```bash
conda env export > environment.yml
```

---

### Example

If you have a file named `cobRa.yml`:

```bash
conda env create -f cobRa.yml
conda activate cobRa
```

---

*Document created to support students and collaborators in the USD MS-ADS program.*

```

---
