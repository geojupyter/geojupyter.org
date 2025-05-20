---
title: "JupyterGIS sync meeting 2025-05-20"
description: |
  A weekly gathering of JupyterGIS team to discuss our progress and help each other out.
  Open to all, but this meeting is _short_ and task-focused, so there will not be time
  for introductions. Please join a core meeting!
date: "2025-05-20"
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

# JupyterGIS sync meeting 2025-05-20

Please add new agenda items under the `New agenda items` heading!

- [Join us on Google Meet](https://meet.google.com/zhk-vygf-gke)
  - [What time is the meeting in my time zone?](https://dateful.com/convert/utc?t=4pm)
- [Previous meetings](https://geojupyter.org/blog/#category=JupyterGIS%20notes)


## Attendees

Your name / GitHub ID / affiliation

* Name / GitHub ID / affiliation
* Matt Fisher / @mfisher87 / Schmidt DSE
* Nicolas Brichet / @brichet / QuantStack
* Arjun Verma / @arjxn-py / QuantStack
* Martin Renou / @martinRenou / QuantStack


## Agenda

* Are we prioritizing work effectively? (For us, and the rest of the community keeping an eye on our progress)
    * Are we looking at the current Milestone to decide what to work on?
    * Does the Milestone page get updated often enough?
    * Matt: I'd like to build a new habit of reviewing our on-deck work together each week. Will Milestones suit that purpose? Or should we have a super-streamlined Project board with a column of issues to pick from? And perhaps do releases more regularly?
        * Example: [JupyterBook project board](https://github.com/orgs/jupyter-book/projects/1)
    * Martin: Totally agree. Project board would feel better. Nice UI to keep track of what's happening. Get rid of current milestone.
* Starting a [team compass](https://compass.geojupyter.org/) - what do you want to see there?
    * Link to the project board
    * Calendar!
    *


### Status reports

* Arjun: Symbology bugfixes!
* Arjun: Autosave changes to layer properties
* Arjun: Bugfix to vectortile layers to support symbology


### Requests for help

* Can we apply graduated and categorized symbology to vectortile layers? https://github.com/geojupyter/jupytergis/issues/704
    * Matt: Trying to do a proof of concept, struggling.
        * Arjun: Try in QGIS to test the dataset.
