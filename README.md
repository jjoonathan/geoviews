[![Travis](https://api.travis-ci.org/ioam/geoviews.svg?branch=master)](https://travis-ci.org/ioam/geoviews)
[![Coveralls](https://img.shields.io/coveralls/ioam/geoviews.svg)](https://coveralls.io/github/ioam/geoviews)
[![Waffle](https://badge.waffle.io/ioam/geoviews.png?label=ready&title=ready)](https://waffle.io/ioam/geoviews)

# GeoViews

GeoViews is a Python library that makes it easy to explore and
visualize geographical, meteorological, and oceanographic datasets,
such as those used in weather, climate, and remote sensing research.

GeoViews is built on the [HoloViews](http://holoviews.org) library for
building flexible visualizations of multidimensional data.  GeoViews
adds a family of geographic plot types based on the
[Cartopy](http://scitools.org.uk/cartopy) library, plotted using
either the [Matplotlib](http://matplotlib.org) or
[Bokeh](http://bokeh.pydata.org) packages.  Each of the new
`GeoElement` plot types is a new HoloViews `Element` that has an
associated geographic projection based on `cartopy.crs`. The
`GeoElements` currently include `Feature`, `WMTS`, `Tiles`, `Points`,
`Contours`, `Image`, and `Text` objects, each of which can easily be
overlaid in the same plots.  E.g. an object with temperature data can
be overlaid with coastline data using an expression like
``gv.Image(temperature)*gv.Feature(cartopy.feature.COASTLINE)``.  Each
`GeoElement` can also be freely combined in layouts with any other
HoloViews `Element`, making it simple to make even complex
multi-figure layouts of overlaid objects.

## Installation

You will first probably want to install iris and/or xarray for working with
multidimensional datasets:

```
conda install -c scitools/label/dev -c conda-forge iris cartopy
conda install xarray
```

You can then install GeoViews and its dependencies using conda:

```
conda install -c ioam holoviews geoviews
```

You can now switch to your preferred working directory, grab a copy of
the notebooks to run locally, and run them using the Jupyter notebook:: 

```
cd ~
python -c 'import geoviews; geoviews.examples("geoviews-examples",include_data=True)'
cd geoviews-examples
jupyter notebook
```
