---
title: "Community Insight: Reproducible Processing Toolbox 🧰"
description: |
  In user interviews, we found that many researchers want to work in a graphical GIS
  environment _and_ a Jupyter Notebook, and they want to come away with a unified,
  reproducible, and shareable product.
date: "2025-07-15"
image: "..."
author:
  - name: "Matt Fisher"
categories:
  - "Community insights"
---

QGIS features
[an excellent **processing toolbox** of geospatial algorithms](https://docs.qgis.org/3.40/en/docs/user_manual/processing/toolbox.html).
This enables researchers to access the computational power of
[GDAL/OGR](https://gdal.org/en/stable/) and other providers without needing to code.
QGIS also provides a
[model builder](https://docs.qgis.org/3.40/en/docs/user_manual/processing/modeler.html)
which enables users to combine processing operations into a single reusable algorithm.
Users can even
[export those algorithms to Python scripts](https://docs.qgis.org/3.40/en/docs/user_manual/processing/modeler.html#exporting-a-model-as-a-python-script)!

ArcGIS provides similar
[geoprocessing](https://pro.arcgis.com/en/pro-app/latest/help/analysis/geoprocessing/basics/find-geoprocessing-tools.htm)
and
[ModelBuilder](https://pro.arcgis.com/en/pro-app/latest/help/analysis/geoprocessing/modelbuilder/what-is-modelbuilder-.htm)
offerings, and while our interviewees have described this as a valuable teaching tool,
they've also commented that a major downside or deal-breaker is the requirement for a
pricey (starting at $700/year at time of writing) ArcGIS license.
Some practitioners described creating tools with the ArcGIS ModelBuilder and then
rewriting them later as open source software packages!
That's a lot of work.

:::{.callout-tip icon=false appearance=minimal}
**We aim to
[create a new workflow](https://github.com/geojupyter/jupytergis/issues/519)
for [JuypterGIS](https://jupytergis.readthedocs.io/), providing an approachable
graphical environment with immediate feedback for geospatial processing operations,
but with tight integration with Jupyter Notebooks.**
:::
