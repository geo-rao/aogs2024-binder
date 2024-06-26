# AOGS-2024-Workshop
This repository comprises notebooks for the AOGS2024 Workshop related to the CMIP6 dataset.

# Getting Started
The notebooks cover:

- accessing the cmip6 dataset from different data sources.
- plotting key variables from the cmip6 dataset.
- producing climate stripes from the accessed cmip6 dataset.

# Requirements
Clone this repository into your local directory.
```
git clone https://github.com/WCRP-CMIP/AOGS-2024-Workshop.git
cd AOGS-2024-Workshop
```
Install and activate the virtual environment **cmip6env** to run the notebooks using Python 3.
```
python3 -m venv cmip6env
source cmip6env/bin/activate
```
Install the requirements.txt file 
```
python3 -m pip install --upgrade pip
pip install -r requirements.txt
```

# Running Notebooks
```
cd notebooks
jupyter lab <notebook>
```

# Python environment with a requirements.txt

[![Binder](http://mybinder.org/badge_logo.svg)](http://mybinder.org/v2/gh/binder-examples/requirements/HEAD)

A Binder-compatible repo with a `requirements.txt` file.

Access this Binder at the following URL

http://mybinder.org/v2/gh/binder-examples/requirements/HEAD

## Notes
The `requirements.txt` file should list all Python libraries that your notebooks
depend on, and they will be installed using:

```
pip install -r requirements.txt
```

The base Binder image contains no extra dependencies, so be as
explicit as possible in defining the packages that you need. This includes
specifying explicit versions wherever possible.

If you do specify strict versions, it is important to do so for *all*
your dependencies, not just direct dependencies.
Strictly specifying only some dependencies is a recipe for environments
breaking over time.

[pip-compile](https://github.com/jazzband/pip-tools/) is a handy
tool for combining loosely specified dependencies with a fully frozen environment.
You write a requirements.in with just the dependencies you need
and pip-compile will generate a requirements.txt with all the strict packages and versions that would come from installing that package right now.
That way, you only need to specify what you actually know you need,
but you also get a snapshot of your environment.

In this example we include the library `seaborn` which will be installed in
the environment, and our notebook uses it to plot a figure.
