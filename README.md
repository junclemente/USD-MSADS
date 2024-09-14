# Masters of Science in Applied Data Science - University of San Diego


This repository is where I have files and references that I can share for anyone who finds them useful. 

For the most part, these are some of the notes that I refer to on a regular basis. 

## Courses

Spring 2024
- ADS 500A - Probability and Statistics for Data Science
- ADS 500B - Data Science Programming 

Summer 2024
- ADS 501 - Foundations of Data Science and Data Ethics
- ADS 502 - Applied Data Mining

Fall 2024
- ADS 505 - Applied Data Science for Business 
- ADS 506 - Applied Time Series Analysis

Spring 2025
- ADS 507 - Practical Data Engineering
- ADS 508 - Data Science with Cloud Computing

Summer 2025
- ADS 503 - Applied Predictive Modeling
- ADS 504 - Machine Learning and Deep Learning for Data Science

Fall 2025
- ADS 509 - Applied Text Mining
- ADS 599 - Capstone Project

## Custom functions

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
