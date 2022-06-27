# python_demo
Demonstrations of common Python data science and geoscience workflows.

Instructions are written in shorthand, and meant to accompany a live demo.

# How do I use Python?

## Virtual environments with conda
You can install different Python packages onto your computer, but sometimes you need different versions of the same package for different projects. "Virtual environments" are distinct profiles you can use in the command line, each with their own Python version and packages. Conda/Anaconda/Miniconda is a commonly used virtual environment manager. I prefer Miniconda. Download and use by following the [Documentation](https://docs.conda.io/en/latest/miniconda.html).

> **Live Demo**
>
> Install Miniconda and make a conda environment containing numpy.
>

1. Install Miniconda

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
conda config --set auto_activate_base false
```

2. Create a virtual environment and use it to install numpy
```
conda create --name demo_env python=3.8
conda activate demo_env
conda install numpy
```

3. Verify that numpy works
```
python
import numpy as np
x = np.array([1, 1, 1, 1])
y = 2.0
print(x * y)
```

## The Visual Studio Code IDE
VSCode is an open source (-ish. It's tied fairly tightly to Microsoft) text editor with excellent support for programming Python. Download [here](https://code.visualstudio.com/download).

> **Live Demo**
>
> Download and install VSCode.
>

## iPython notebooks versus python scripts
You can write your own programs with the `.py` extension, and execute them with the Python interpreter from the command line.

Alternatively, you can use the `.ipynb` to make iPython (Jupyter) notebooks. Jupyter notebooks are better for making plots, but normal Python scripts have better debugging support.

> **Live Demo**
>
> Make a "hello_world.py" script in Python using a function.
> Put the equivalent functionality in an iPython notebook.
>

## Debugging with pdb or VSCode’s visual debugging tools
You can and should debug with breakpoints. In Python 3, you can use the `breakpoint` command to stop code execution and open an interactive interpreter. In VSCode, you can also set a visual breakpoint.

> **Live Demo**
>
> Modify `hello_world.py` to add a variable that gets changed.
> Use `breakpoint()` funtion to examine memory from the command line.
> Set a visual breakpoint in VSCode to examine memory using the visual debugger.

## Finding inclusive & approachable sources of help
Most large projects have forums or Discord channels. StackOverflow is your friend. Asking a question is hard -- as Socrates famously wrote, "to ask a question on StackOverflow with sufficient detail for a useful response, one must already know the answer", or something like that. People will often ask for more information, and that's not a big deal. Folks generally try to be very polite when asking or answering.

# Common data science workflows

> **Live Demo**
>
> Install numpy, pandas, matplotlib, xarray, and geoviews.
> Use Numpy to create a fake dataset of phytoplankton concentration across latitude and longitude.
> Use Pandas to label the dataset.
> Use matplotlib to plot an image of the dataset.
> Use geoviews to plot the image on a fancy interactive globe.
> Use xarray to save the dataset to a Zarr store.

## Pandas
## Numpy
## SciPy
## Matplotlib
## Visualization with xarray, holoviews, geoviews, and bokeh
### Including how to never, ever use NetCDF files and their draconian suite of command line tools ever again

# Snazzy Python language features to make your mentor say “ooh! You’re so good at Python!”
## List comprehensions
## Dictionaries, and dictionary comprehensions
## Decorators
## Context managers
## Generators

# Managing a Python project
## How to structure code into a module or package
## Using git to install open source packages
## Making your environment reproducible with a pyproject.toml file

# Machine learning
## Classical ML with scikit-learn
## Deep learning with PyTorch
## Fancy deep learning with PyTorch Lightning

# Your Questions:
## How do I use [fancy confusing library I’ve been asked to use]?
## Got any pointers on my code?
