---
title: "JupyterGIS sync meeting 2025-05-06"
description: |
  A weekly gathering of JupyterGIS team to discuss our progress and help each other out.
  Open to all, but this meeting is _short_ and task-focused, so there will not be time
  for introductions. Please join a core meeting!
date: "2025-05-06"
image: "/assets/images/standup.jpg"
author:
  - name: "The GeoJupyter community"
categories:
  - "JupyterGIS notes"
tags: [jupytergis-notes]
---

:::info {.callout-info}
:mag: This meeting is _short_ and _task-focused_. Unfortunately, we won't have time to
introduce every new person to the team. Please attend core community meetings ([see
GeoJupyter calendar](https://geojupyter.org/calendar)) to meet the team and add your own
agenda items, and/or
[introduce yourself on Zulip](https://jupyter.zulipchat.com/#narrow/channel/471314-geojupyter/topic/Welcome)!
:::

# JupyterGIS sync meeting 2025-05-06

Please add new agenda items under the `New agenda items` heading!

- [Join us on Google Meet](https://meet.google.com/zhk-vygf-gke)
  - [What time is the meeting in my time zone?](https://dateful.com/convert/utc?t=4pm)
- [Previous meetings](https://geojupyter.org/blog/#category=JupyterGIS%20notes)


## Attendees

Your name / GitHub ID / affiliation

* Matt Fisher / @mfisher87 / DSE
* Arjun Verma / @arjxn-py / QuantStack
* Martin Renou / @martinRenou / QuantStack
* Greg Mooney / @gjmooney / QuantStack


## Status reports

* Matt: CNG went well! Prepping for a workshop next week, won't be doing much dev.
* Arjun:
    * Settings PR: <PR Link>
    * Schema version PR: https://github.com/geojupyter/jupytergis/pull/590
        * Should the field be under "metadata" or at the root?
        * ipynb has "nbformat" and "nbformat_minor" both at the root.
            * Notebook metadata has information about the kernel, that's it.
            * Maybe JGIS projects have "author", "last_edited" as metadata. What else?
            * What about viewport location? Currently in `options`, which we think makes sense. That's the project _data_.
            * **Decision**: Keep `schema_version` at the root!
        * What about annotations? Should they be metadata or top-level?
            * Matt/Greg: Gut says top-level, but we can leave as-is for now.
    * Annotation UX improvements: <PR Link>
* David:
    * TiTiler extension: https://github.com/geojupyter/jupytergis-tiler
        * Serve zarr file https://github.com/geojupyter/jupytergis-tiler/blob/main/examples/xarray.ipynb
        * Does this enable collaboration on a Xarray DataArray?
            * Depends. if the Kernel is shared by everyone, it should work!
            * If JupyterLite, no go.
        * Adds new dependency, makes the doc a bit more complex.
        * Not sure whether this belongs in core yet. David feels strongly not to! Martin feels adding to core could be nice.
        * Serve non-optimized GeoTIFFs from kernel.

## Requests for help

None today!
