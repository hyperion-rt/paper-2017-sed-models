### About

This directory contains supplementary materials for the following publication:

Robitaille, 2017, *A modular set of synthetic spectral energy 
distributions for young stellar objects*

The models themselves are available on [Zenodo](https://doi.org/10.5281/zenodo.166732) in a form usable by the SED fitting code. You can also find the raw Hyperion input/output files [here](https://doi.org/10.5281/zenodo.572233).

To get started, take a look at [this Jupyter notebook](https://github.com/hyperion-rt/paper-2017-sed-models/blob/master/notebook/using_the_models.ipynb) to find out more about how to use the models.

### Requirements

The packages required to run the scripts in this directory are:

* Python 2.7 or 3.3 or later (http://www.python.org)
* Numpy 1.10 or later (http://www.numpy.org)
* Matplotlib 1.4 or later (http://matplotlib.sourceforge.net)
* Astropy 1.0 or later (http://www.astropy.org)
* Jupyter notebook (https://jupyter-notebook.readthedocs.io)
* sedfitter 1.0 or later (http://sedfitter.readthedocs.io/en/stable/)

### Questions/Issues

For any questions or issues with using the models, please [open an issue](https://github.com/hyperion-rt/paper-2017-sed-models/issues/new) in this repository. For issues with using the [sedfitter](https://github.com/astrofrog/sedfitter) Python package, [open an issue](https://github.com/astrofrog/sedfitter/issues/new) in the repository for that package.

### FAQs

**What is the value of r_0 in the paper?**

There was an oversight in the paper which meant that the value of r_0 was not given. It is set to 1000 au.

**How can I find out what the dust sublimation radius is for each model?**

There is currently no table of r_sub values for each model, but you can find this out by downloading the Hyperion input/output files for the models you are interested in [from here](https://doi.org/10.5281/zenodo.572233) and then use code along the lines of:

    >>> from hyperion.model import ModelOutput
    >>> from hyperion.util.constants import au
    >>> mo = ModelOutput('grids-1.1/s---s-i/output/a3/A3kQmQtj.rtout')
    >>> grid = mo.get_quantities()
    >>> grid.r[1] / au
    0.0023819780734823503

to find out the r_sub radius in au for each model.

### Future plans

This repository will evolve over time. In particular, I may:

* Add the scripts to reproduce the results from the paper
* Add the scripts used to construct, run, and post-process the model grid

To get announcements when these are made available, you can sign up to the following mailing list:

https://groups.google.com/forum/#!forum/protostars

Note that you do not need a Google account, and can sign up by sending an empty email to:

protostars+subscribe@googlegroups.com

### Contact

For any questions, please [open an 
issue](https://github.com/hyperion-rt/paper-2017-sed-models/issues) in 
this repository.
