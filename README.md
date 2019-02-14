# gridded_data

Repo for "Workflows for gridded climate datasets" waterhackweek tutorial

## Run tutorial notebooks in the cloud

By far the easiest way to run the notebooks that are part of this tutorial is to click the **launch binder** button. This will use the binder service made available by [pangeo](https://binder.pangeo.io) to create a docker container based on this repository and launch it in the cloud. Don't worry if this does not mean anything to you. Just hit the button:
 
[![Binder](https://binder.pangeo.io/badge.svg)](https://binder.pangeo.io/v2/gh/bartnijssen/gridded_data/binder)

If you do want to install the notebooks locally or in your , then by all means follow the instructions below. In that case you want to use the `master` branch rather than the binder branch.

## conda environment and jupyter

- The conda environment file `environment.yml` doesn't install jupyter. It assumes that you already have conda installed (or miniconda) and a working setup for running jupyter notebooks. To create a conda environment named `whw_gridded_data` from this file: `conda env create -f environment.yml`

- To install that environment as a kernel in your jupyter setup:
  `conda activate whw_gridded_data; ipython kernel install --user --name whw_gridded_data`

### Install miniconda and setup jupyter lab
Steps taken from https://geohackweek.github.io/preliminary/01-conda-tutorial/
Instructions for MacOSX (and Windows?) are also available there.

**On linux:**
```bash
# Install miniconda
url=https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
wget $url -O miniconda.sh
bash miniconda.sh -b -p $HOME/miniconda3
export PATH="$HOME/miniconda3/bin:$PATH"
conda update conda --yes

# Create a conda environment with jupyterlab
conda create -n jupyterlab -c conda-forge python=3.6 jupyterlab nb_conda_kernels

# Starting jupyter lab
conda activate jupyterlab
# If that doesn't work, try source activate jupyterlab
jupyter lab
```


## Other WaterHackWeek resources
- https://waterhackweek.github.io/
- https://www.cuahsi.org/education/cyberseminars/waterhackweek-cyberseminar-series/
