---
title: "GeoJupyter virtual hackathon 2025-06-25"
description: |
  A GeoJupyter virtual hackathon. Open to all!
date: "2025-06-25"
image: "/assets/images/hackathon.jpg"
author:
  - name: "The GeoJupyter community"
categories:
  - "Hackathons"
tags: [hackathons]
---

# GeoJupyter virtual hackathon 2025-06-25

Please add new agenda items under the `New agenda items` heading!

- [Join us on Zoom](https://berkeley.zoom.us/j/92451699568)
  - [What time is the meeting in my time zone?](https://dateful.com/convert/utc?t=3pm)
- [Notes from previous hackathons](https://geojupyter.org/blog/#category=Hackathons)
- [GeoJupyter](https://geojupyter.org) handy links:
  - [GitHub org](https://github.com/geojupyter)
  - [Community calendar](https://geojupyter.org/calendar.html)
  - [Zulip chat](https://jupyter.zulipchat.com/#narrow/channel/471314-geojupyter)


## Sign in!

Your name / GitHub ID / affiliation

* Kristin Davis / @kpdavi  / Schmidt DSE
* Martin Renou / @martinRenou / QuantStack
* Matt Fisher / @mfisher87 / Schmidt DSE
* Kirstie Whitaker / @KirstieJAne / Berkeley Institute for Data Science


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

* [Symbology menu overhaul](https://github.com/geojupyter/jupytergis/pull/754)
* Idea 2
* Idea 3


### 🪄 (all the minutes) Hack together!

Form teams from the ideas generated in the step above!


#### Breakout rooms

* Lobby: Symbology



### 💬 (10 minutes) Share out

Think about:
What exciting things did you accomplish?
What loose ends remain?
Big questions? Big ideas?

Please write for people who don’t have full context; link to related issues and documentation!

* Symbology
    * Plan to use [Vega Expressions](https://vega.github.io/vega/docs/expressions/) instead of OpenLayers in the vectorlayer.json - open an issue for this!
    * Could use the descriptions around symbology information developed / described by [Sam (software engineer at DSE)](https://interactivedatascience.courses/) to inform how the schema is structured and / or described
        * Let Sam know his data visualization class slides are 404ing
    * Have some example project files bundled with the project and want to validate that they're obeying the schemas in CI - every time a PR is opened, want to make sure those aren't broken
    * Need to improve heatmap schema - maybe in the next PR
    * Think about the schema levels of abstraction -- should we extract symbology schemas into their own schema sub-directory instead of bundling them with the layers schemas? This will be especially important once we start discriminating between point, line, and polygon sub-types of vector layers because we'll have an explosion of schema possibilities and we'll want to drive the form generation more from the schema and less from the JavaScript.
    * How to do JSONSchema definitions and reference them _across files_?
    * Consider `creationform.tsx` -> `layerCreationForm.tsx`?
    * Next steps:
        * Create new form class that inherits from baseform, symbologyForm.
        * Move logic from symbologyDialog -> the new symbologyForm base component.
        * A starting point may be to use BaseForm in the SymbologyDialog module.
            * Look at creationform and debug/log to see what we pass to LayerForm on line 220 to better understand the implementation.
        * MAY need to register our schema in the formSchemaRegistry!
            * There's a `registerSchema` function, but it seems we never call it? Is it dynamically called in the generated code?
* TODO: Form property `syncData` -> `submitCallback`?
* TODO: Docs on schema -> TS/Py types generation
* Share out 2
* ...
