---
title: "JupyterGIS sync meeting 2025-04-01"
description: |
  A weekly gathering of JupyterGIS team to discuss our progress and help each other out.
  Open to all, but this meeting is _short_ and task-focused, so there will not be time
  for introductions. Please join a core meeting!
date: "2025-04-01"
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

# JupyterGIS sync meeting 2025-04-01

Please add new agenda items under the `New agenda items` heading!

- [Join us on Google Meet](https://meet.google.com/zhk-vygf-gke)
  - [What time is the meeting in my time zone?](https://dateful.com/convert/utc?t=4pm)
- [Previous meetings](https://geojupyter.org/blog/#category=JupyterGIS%20notes)


## Attendees

Your name / GitHub ID / affiliation

* Matt Fisher / @mfisher87 / Schmidt DSE
* Arjun Verma / @arjxn-py / QuantStack
* Greg Mooney / @gjmooney / QuantStack
* Martin Renou / @martinRenou / QuantStack


## Status reports

* Matt & Arjun: "Save as..." https://github.com/geojupyter/jupytergis/issues/582
* Arjun:
    * Restored local GeoTIFFs!
    * Modular processing logic - SQL query focused
    * Saving processing outputs as separate files instead of embedding in JGIS project.
      * Martin: How about making it optional to embed the processed data in jgis? With a checkbox in the processing form?
    * Streamlining docs build -- 1 conda environment
    * Reprojection command
* Matt: `geo_debug` function

## Requests for help

* Want to implement "Save as..." in the Python API & UI.
  How to share functionality / call between Python & JS?
  * Save as JGIS & Save as QGIS could be in same UI menu.
  * Write separate JS and Python implementations
  * In JS implementation, "Save as..." should rename (implemented in documentmanager) the existing document, and create a copy with the old name.

## Misc

* Package JGIS data files with project data in a tar file? [Can untar in JS](https://github.com/emscripten-forge/untarjs)!
*
