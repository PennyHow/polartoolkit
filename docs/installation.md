# Installation
Here I use mamba to install packages, but conda should work as well:

## Create a new python environment:

    mamba create --name antarctic_plots python=3.9 
    mamba activate antarctic_plots

## install the package: 

    pip install antarctic-plots

This will install most of the dependencies, except for geopandas, which you'll need to install seperately

    mamba install geopandas

You may need to re-install pygmt

    mamba install pygmt

## To install the latest development version from Github:

    git clone https://github.com/mdtanker/antarctic_plots.git
    cd antarctic_plots
    pip install -e .

Test the install by running the first few cells of [examples/examples.ipynb](https://github.com/mdtanker/antarctic_plots/blob/main/examples/examples.ipynb) or the equivalent [.py file](https://github.com/mdtanker/antarctic_plots/blob/main/examples/examples.py)

If you get an error related to traitlets run the following command as discuss [here](https://github.com/microsoft/vscode-jupyter/issues/5689#issuecomment-829538285):

    conda install ipykernel --update-deps --force-reinstall


<!-- ## Older instructions
## install the dependencies seperately:
    
    mamba install pandas numpy pooch xarray pyproj verde rioxarray pygmt geopandas netCDF4 tqdm

Optionally add ipykernel jupyterlab and notebook if you want to use iPython.

## to import working env into poetry
    mamba create --name antarctic_plots python=3.8
    mamba activate antarctic_plots
    mamba install pandas numpy pooch xarray pyproj verde rioxarray netCDF4 pygmt geopandas black pytest flake8 isort jupyter-book
    pip list --format=freeze > requirements.txt
    cat requirements.txt | xargs poetry add
    pip insteal -e . 

## to get poetry to work
without hashes
    poetry export -f requirements.txt --output requirements.txt --dev --without-hashes
    pip install -r requirements.txt

or with hashes
    poetry export -f requirements.txt --output requirements.txt --dev 
    pip install --no-deps -r requirements.txt

pip install -e .
conda install pygmt geopandas -->