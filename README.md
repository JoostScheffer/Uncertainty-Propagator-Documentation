# Uncertainty-Propagator-Documentation

Welcome to the Uncertainty-documentation repository! This repository contains the spinx project used to build the documentation
for the [Uncertainty-Propagator project](https://github.com/JoostScheffer/Uncertainty-Propagator/tree/main).

If you are looking for a quick way to get going [go here](https://github.com/JoostScheffer/Uncertainty-Propagator/blob/main/README.md)

## Building the documentation

If you want to build the documentation this can be done very easily using `spinx` using the following code

```bash

# Create an environment to build the docs in
python3 -m venv .venv
source .venv/bin/activate  # For linux
.venv/Scripts/Activate.bat  # For windows
pip install -r requirements.txt

# Now all that is left is build the docs!
make html

```

## Updating the documentation

If only the docstrings of the code have changes no rebuild of the rst files is needed. If for example some new classes or modules have been
added run the following code to update the rst files:

```bash

shinx-apidoc -o source Uncertainty-Propagator/src/uncertainty_propagator

```