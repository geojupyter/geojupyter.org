---
title: "JupyterGIS sync meeting 2025-03-04"
description: |
  A weekly gathering of JupyterGIS team to discuss our progress and help each other out.
  Open to all, but this meeting is _short_ and task-focused, so there will not be time
  for introductions. Please join a core meeting!
date: "2025-03-04"
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

# JupyterGIS sync meeting 2025-03-04

Please add new agenda items under the `New agenda items` heading!

- [Join us on Google Meet](https://meet.google.com/zhk-vygf-gke)
  - [What time is the meeting in my time zone?](https://dateful.com/convert/utc?t=4pm)
- [Previous meetings](https://geojupyter.org/blog/#category=JupyterGIS%20notes)


## Attendees

Your name / GitHub ID / affiliation

* Matt / @mfisher87 / Schmidt DSE
* Greg / @gjmooney / QuantStack
* Martin / @martinRenou / QuantStack
* Arjun / @arjxn-py / QuantStack


## Status reports

* Martin: Not much coding news. Blog post is live! QuantStack slowing down (Arjun still on project).
* Arjun: Processing proof-of-concept. Initially using GDAL WASM under the hood. Create a buffer on vector layer. Building a form to let the user customize the operation.
    * https://github.com/geojupyter/jupytergis/pull/510
    * Reproducibility!
    * QGIS using GDAL under the hood
        * It sometimes provides the underlying GDAL commands in the processing GUI
        * Build a JSON schema for GDAL commands
        * This schema would generate Typescript & Python interfaces
        * This will help with form generation
        * Could also enable generation of Python code (GDAL Python bindings)
        *
* Status


## Requests for help

* In-person hackathon & QuantStack participation
    * Continue discussion on Zulip!
* Funding more QuantStack work
    * QuantStack definitely interested.
    *
* Help request
