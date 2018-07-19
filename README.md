# Jupyter Notebooks for Altair

This repository contains tutorial and example Jupyter Notebooks for Altair.

You can browse static version of these notebooks here on GitHub, or click the `binder`
badge below to launch of live Jupyter Notebook server with the notebooks in this 
repo.

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/adrienpacifico/altair/master?filepath=https%3A%2F%2Fgithub.com%2Fadrienpacifico%2Faltair_notebooks%2Fblob%2Fmaster%2Fnotebooks%2F01-Index.ipynb)

## Example

Here is an example using Altair to quickly visualize and display a dataset with the native Vega-Lite renderer in the JupyterLab:

```python
import altair as alt

# to use with Jupyter notebook (not JupyterLab) run the following
# alt.renderers.enable('notebook')

# load a simple dataset as a pandas DataFrame
from vega_datasets import data
cars = data.cars()

alt.Chart(cars).mark_point().encode(
    x='Horsepower',
    y='Miles_per_Gallon',
    color='Origin',
)
```

![Altair Visualization](images/cars.png?raw=true)
