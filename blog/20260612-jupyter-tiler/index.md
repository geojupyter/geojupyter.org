---
title: "Announcing jupyter-tiler!"
description: |
  [jupyter-tiler](https://jupyter-tiler.readthedocs.io/) is a backend tool to enable use
  of dynamic tile servers (currently supporting [TiTiler](https://titiler.xyz/) or
  [Xpublish](https://xpublish.readthedocs.io)) within the Jupyter architecture.
date: "2026-06-12"
# image: "TODO.jpg"
author:
  - name: "Matt Fisher"
categories:
  - "Announcements"
---

When Geospatial professionals work with gridded data in Python, they often reach for
[xarray](https://docs.xarray.dev).
Xarray provides clear labeling of dimensions and variables, efficient data loading,
scalability, support for cloud-native data formats, and a rich ecosystem that enables
users to write readable and fast data analysis code.

However, users commonly face challenges when it comes time to visualize their data in
xarray DataSets.
While it's relatively easy for users to create static plots, interactively visualizing
and exploring that data is unintuitive.
A common approach is to "simply" write the dataset, or a slice of the dataset, out to a
file and visualizing the data in [QGIS](https://qgis.org/).
In addition to the friction and context-switching caused by using multiple tools,
writing the data out to a file opens a whole new set of questions around
[file formats](https://guide.cloudnativegeo.org/).

Ideally, the user would be able to interactively explore their dataset without leaving
the Jupyter Notebook interface -- **this is the problem that
[jupyter-tiler](https://jupyter-tiler.readthedocs.io/) solves**!


## jupyter-tiler in JupyterGIS

jupyter-tiler has been integrated with [JupyterGIS](https://jupytergis.readthedocs.io/),
enabling easy interactive visualization of your xarray data with one function call:

```python
await jgis_document.add_data_array_layer(
    name="Digital elevation model layer",
    data_array=xarray_dataarray_dem,
    colormap_name="terrain",
    colormap_range=(
        int(xarray_dataarray_dem.min().compute()),
        int(xarray_dataarray_dem.max().compute()),
    )
```

![jupyter-tiler in JupyterGIS, in action](./jupyter-tiler-in-jupytergis.mp4){loop="true" autoplay="true" muted="true"}


## How jupyter-tiler works

![A diagram showing how jupyter-tiler enables Jupyter interactive map widgets to dynamically serve tiles of xarray data](https://jupyter-tiler.readthedocs.io/en/latest/_images/high-level-diagram.svg)

_TODO_


## How jupyter-tiler was made

jupyter-tiler started life as
[jupytergis-tiler](https://github.com/geojupyter/jupytergis-tiler), a very similar
library by [David Brochart](https://github.com/davidbrochart) that is specific to
JupyterGIS.
