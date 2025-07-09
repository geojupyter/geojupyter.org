---
title: "GeoJupyter virtual hackathon 2025-07-09"
description: |
  A GeoJupyter virtual hackathon. Open to all!
date: "2025-07-09"
image: "/assets/images/hackathon.jpg"
author:
  - name: "The GeoJupyter community"
categories:
  - "Hackathons"
tags: [hackathons]
---

# GeoJupyter virtual hackathon 2025-07-09

Please add new agenda items under the `New agenda items` heading!

- [Join us on Zoom](https://berkeley.zoom.us/j/92451699568)
  - [What time is the meeting in my time zone?](https://dateful.com/convert/utc?t=2pm)
- [Notes from previous hackathons](https://geojupyter.org/blog/#category=Hackathons)
- [GeoJupyter](https://geojupyter.org) handy links:
  - [GitHub org](https://github.com/geojupyter)
  - [Community calendar](https://geojupyter.org/calendar.html)
  - [Zulip chat](https://jupyter.zulipchat.com/#narrow/channel/471314-geojupyter)


## Sign in!

Your name / GitHub ID / affiliation

* Matt Fisher / @mfisher87 / DSE
* Martin Renou / @martinRenou / QuantStack
* Florence Haudin /@HaudinFlorence / QuantStack
* Jason Grout / GitHub ID / Independent


## Agenda & notes

### ⚡ (5 minutes) Lightning intros

Tell us about you in 30 seconds or less!


### 🌐 (5 minutes) Lightning demo

What's new? Show & tell.
Post on Zulip to request a show & tell slot;
by default, QuantStack will demo awesome JupyterGIS progress each meeting!


### 💡 (5 minutes) What will we hack on?

* **What do you want to work on today**?
  * For ideas, check out the [hackathon](https://github.com/geojupyter/jupytergis/labels/hackathon)
    and [good first issue](https://github.com/geojupyter/jupytergis/labels/good%20first%20issue)
    labels on the JupyterGIS project!
* **Add your ideas to the “ideas” list below**.
* **Add your favorite emoji or a `+` next to ideas you’re excited about**.
  * Press the colon (:) key on your keyboard or navigate to “Insert > Emoji” in the menu bar to open the emoji browser.


#### Ideas

* More robustly defining the symbology schemas and generating those forms from the schemas (https://github.com/geojupyter/jupytergis/pull/754)
* Support vector layer sub-types (polygon, line, point)


### 🪄 (all the minutes) Hack together!

Form teams from the ideas generated in the step above!


#### Breakout rooms

None today, all together!


### 💬 (10 minutes) Share out

Think about:
What exciting things did you accomplish?
What loose ends remain?
Big questions? Big ideas?

Please write for people who don’t have full context; link to related issues and documentation!

* Separate the RJSF schema pre-processing (creating forms.json) into a separate NPM script
    * "forms.json is legacy code" -- from before we had a registry of json schemas. Now that we have a registry, we could get rid of it! Consider generating the schema registry from the source files, dereferencing on the fly if needed.
    * Matt will document this :)
* Vector sub-types: When adding a layer that has multiple types, create a group of layers instead of displaying a QGIS-ish dialog allowing the user to select from the available types. (Maybe we implement that later!)
