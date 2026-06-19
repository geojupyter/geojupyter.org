---
title: "Announcing jupyter-tiler!"
description: |
  [jupyter-tiler](https://jupyter-tiler.readthedocs.io/) enables users of Jupyter
  interactive map widgets (like JupyterGIS) to visualize large raster datasets without
  switching tools or worrying about file formats by leveraging dynamic tile servers
  under the hood (currently supporting [TiTiler](https://titiler.xyz/) or
  [Xpublish](https://xpublish.readthedocs.io)).
date: "2026-06-22"
image: "thumbnail.jpg"
author:
  - name: "Matt Fisher"
    orcid: "0000-0003-3260-5445"
categories:
  - "Announcements"
---

When users of geospatial data computate with raster data, they often face
challenges with visualizing their results.
A typical workflow involves first reading data into an analysis tool like
[xarray](https://docs.xarray.dev/en/stable/), then performing computations on the data,
then visualizing their results. This analysis ↔ visualization cycle is usually repeated
many times.

While users can easily produce static plots of their raster dataset, they usually really
need interactive visualizations to effectively explore their results.
Interactive visualization often requires writing data to disk, decisions about
visualization-friendly [file formats](https://guide.cloudnativegeo.org/), and/or
[context-switching](https://en.wikipedia.org/wiki/Human_multitasking) to another tool
(like [QGIS](https://qgis.org)).

**[jupyter-tiler](https://jupyter-tiler.readthedocs.io/) helps those users create
interactive visualizations of their computation results without leaving the Notebook
environment or writing files, eliminating costly decision-making and context switches**.


## jupyter-tiler in JupyterGIS

jupyter-tiler has been integrated with [JupyterGIS](https://jupytergis.readthedocs.io/),
streamlining interactive visualization of xarray `DataArray`s to a single function call:

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

![jupyter-tiler in JupyterGIS, in action: The user runs two Notebook cells which add xarray `DataArray`s `da_dem` (a Digital Elevation Model) and `da_acc` (a flow accumulation model) to the map, each in one step. The tile server handles displaying the data at the optimal resolution depending on the user's zoom level.](./jupyter-tiler-in-jupytergis.mp4){fig-alt="A user executes 2 Jupyter Notebook cells, similar to the above, to add two new layers from xarray DataArrays to the map: a digital elevation model and a flow accumulation model. After the cells are executed, the data is visualized on an interactive map. The user zooms in to the map, showing jupyter-tiler dynamically loading map tiles at the appropriate resolutions." loop="true" autoplay="true" muted="true"}


## How jupyter-tiler works

![A diagram showing how jupyter-tiler enables Jupyter interactive map widgets to dynamically serve tiles of xarray data](https://jupyter-tiler.readthedocs.io/en/latest/_images/high-level-diagram.svg){fig-alt="A diagram shows a data flow: A third-party interactive map widget leverages jupyter-tiler to display data on the map. First, the widget tells the jupyter-tiler API to add a `DataArray` layer. jupyter-tiler then tells TiTiler to add a `DataArray` route to its HTTP API. This triggers jupyter-server-proxy to expose that route through Jupyter Server. The map widget receives a URL it can use to request tiles. And finally, the map widget uses that URL to request and receive tiles from TiTiler via jupyter-server-proxy."}

jupyter-tiler works in the back-end, and it's intended for use by authors of Jupyter
interactive map widgets, like
[ipyleaflet](https://github.com/jupyter-widgets/ipyleaflet),
[ipyopenlayers](https://github.com/geojupyter/ipyopenlayers), and JupyterGIS, to enable
them to expose convenient features that leverage a dynamic tile server to their users.

It provides a [Python
API](https://jupyter-tiler.readthedocs.io/en/latest/user-guide/reference/api/)
for interacting with a dynamic tile server (currently supporting both
[TiTiler](https://titiler.xyz/) or [Xpublish](https://xpublish.readthedocs.io)).
You hand off an xarray `DataArray` and some options, jupyter-tiler sets up the tile server
for you, and returns a URL template that you can directly display with a Javascript
interactive map (Leaflet, OpenLayers, MapLibre, etc.).

jupyter-tiler also provides a proxy
([jupyter-server-proxy](https://github.com/jupyterhub/jupyter-server-proxy))
to enable usage of jupyter-tiler in cloud environments (like JupyterHub) without extra
deployment complexity.
As a user, you don't need to think about ports; just use the URL that jupyter-tiler
returns to you.


## How jupyter-tiler was made

jupyter-tiler started life as
[jupytergis-tiler](https://github.com/geojupyter/jupytergis-tiler), a very similar
library by [David
Brochart](https://github.com/davidbrochart) at [QuantStack](https://quantstack.net/)
that is specific to JupyterGIS.
You can read more about jupytergis-tiler in its own
[announcement blog post](https://medium.com/@david-brochart/create-your-own-layers-in-jupytergis-cbb995a89b16)!

In jupytergis-tiler, David implemented an in-kernel tile server that could directly read
data from an xarray `DataArray` and serve tiles using TiTiler.

I built jupyter-tiler as a generalization of jupytergis-tiler so that this architecture
could be used by any Jupyter interactive map widget.
I also added support for multiple dynamic tiling backends (currently, TiTiler and
Xpublish).


## Try it!

You can try jupyter-tiler with JupyterGIS by installing the optional `tiler` dependency
group:

```bash
pip install jupytergis[tiler]
```
