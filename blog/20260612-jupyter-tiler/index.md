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

When geospatial professionals work with gridded data in Python, they often reach for
[xarray](https://docs.xarray.dev).
Xarray provides clear labeling of dimensions and variables, efficient data loading,
scalability, support for cloud-native data formats, and a rich ecosystem that enables
users to write readable and fast data analysis code.

However, users commonly face challenges when it comes time to visualize their data in
xarray DataSets.
While it's relatively easy for users to create static plots, interactively visualizing
and exploring that data is unintuitive -- this isn't one of xarray's design goals.
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
)
```

![jupyter-tiler in JupyterGIS, in action](./jupyter-tiler-in-jupytergis.mp4){fig-alt="A user executes 2 Jupyter Notebook cells, similar to the above, to add two new layers from xarray DataArrays to the map: a digital elevation model and a flow accumulation model. After the cells are executed, the data is visualized on an interactive map. The user zooms in to the map, showing jupyter-tiler dynamically loading map tiles at the appropriate resolutions." loop="true" autoplay="true" muted="true"}


## How jupyter-tiler works

![A diagram showing how jupyter-tiler enables Jupyter interactive map widgets to dynamically serve tiles of xarray data](https://jupyter-tiler.readthedocs.io/en/latest/_images/high-level-diagram.svg){fig-alt="A diagram shows a data flow: A third-party interactive map widget leverages jupyter-tiler to display data on the map. First, the widget tells the jupyter-tiler API to add a DataArray layer. jupyter-tiler then tells TiTiler to add a DataArray route to its HTTP API. This triggers jupyter-server-proxy to expose that route through Jupyter Server. The map widget receives a URL it can use to request tiles. And finally, the map widget uses that URL to request and receive tiles from TiTiler via jupyter-server-proxy."}

jupyter-tiler works in the back-end, and it's intended for use by authors of Jupyter
interactive map widgets, like
[ipyleaflet](https://github.com/jupyter-widgets/ipyleaflet),
[ipyopenlayers](https://github.com/geojupyter/ipyopenlayers), and JupyterGIS, to enable
them to expose convenient features that leverage a dynamic tile server to their users.

It provides a [Python
API](https://jupyter-tiler.readthedocs.io/en/latest/user-guide/reference/api/)
for interacting with a dynamic tile server (currently supporting both
[TiTiler](https://titiler.xyz/) or [Xpublish](https://xpublish.readthedocs.io)).
You hand off an xarray DataArray and some options, jupyter-tiler sets up the tile server
for you, and returns a URL template that you can directly display with a Javascript
interactive map (Leaflet, OpenLayers, MapLibre, etc.).

jupyter-tiler also provides a proxy
([jupyter-server-proxy](https://github.com/jupyterhub/jupyter-server-proxy))
to enable usage of jupyter-tiler without extra deployment complexity.
As a user, you don't need to think about ports; just use the URL that jupyter-tiler
returns to you.


## How jupyter-tiler was made

jupyter-tiler started life as
[jupytergis-tiler](https://github.com/geojupyter/jupytergis-tiler), a very similar
library that is specific to JupyterGIS by [David
Brochart](https://github.com/davidbrochart) at [QuantStack](https://quantstack.net/).

David solved the hard technical problems in jupytergis-tiler.
jupyter-tiler is simply a generalization so that this architecture could be used by any
Jupyter interactive map widget, and to support multiple dynamic tiling backends
(currently, TiTiler and Xpublish).
