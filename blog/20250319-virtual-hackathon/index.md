---
title: "GeoJupyter virtual hackathon 2025-03-19"
description: |
  A GeoJupyter virtual hackathon. Open to all!
date: "2025-03-19"
author:
  - name: "The GeoJupyter community"
categories:
  - "Hackathons"
tags: [hackathons]
---

# GeoJupyter virtual hackathon 2025-03-19

Please add new agenda items under the `New agenda items` heading!

- [Join us on Zoom](https://berkeley.zoom.us/j/92451699568)
  - [What time is the meeting in my time zone?](https://dateful.com/convert/utc?t=3pm)
- [Previous hackathons](https://geojupyter.org/blog/#category=Hackathons)
- [GeoJupyter](https://geojupyter.org) handy links:
  - [GitHub org](https://github.com/geojupyter)
  - [Community calendar](https://geojupyter.org/calendar.html)
  - [Zulip chat](https://jupyter.zulipchat.com/#narrow/channel/471314-geojupyter)


## Attendees

Your name / GitHub ID / affiliation / what content (tv, book, course, youtube series, ...) are you enjoying lately?

* Kristin Davis / @kpdavi / Schmidst DSE / Alone Australia
* Matt Fisher / @mfisher87 / Schmidt DSE / Severance!
* Yao-Ting Yao / @YaoTingYao / ClarkCGA / rewatch game of thrones
* Martin Renou / @martinRenou / QuantStack / Elden Ring!
* Arjun Verma / @arjxn-py / QuantStack / The Office :D


## Agenda & notes

### ⚡ (5 minutes) Lightning intros

Tell us about you in 30 seconds or less!


### 🌐 (5 minutes) Lightning demo

What's new? Show & tell.
Post on Zulip to request a show & tell slot; by default, QuantStack will demo awesome
JupyterGIS progress each meeting!


### 💡 (5 minutes) Idea / team forming

* What do you want to work on today?
* Add your ideas to the “Hack teams” section below.
* Add your favorite emoji next to ideas you’re excited about. Press the colon (:) key on your keyboard or navigate to “Insert > Emoji” in the menu bar to open the emoji browser.
* Form teams from the ideas generated in the steps above! Add your objectives to the “Hack teams” section of the doc below.
* Create breakout rooms.


### 🪄 (all the minutes) Hack together!

### 💬 (10 minutes) Share out

* Save your progress in GitHub or Zulip as appropriate!
  Please write for people who don’t have full context; link to related issues and documentation!
* Fill in the “Share out” section of the doc below.


## Hack teams

For ideas, check out the [hackathon](https://github.com/geojupyter/jupytergis/labels/hackathon) and [good first issue](https://github.com/geojupyter/jupytergis/labels/good%20first%20issue) labels on the JupyterGIS project!

Join the corresponding breakout room to hack!

1. Add units to buffer menu +++
2. Identify tool doesn't indicate when no layer selected ++
3. Other "good first issue" ++
4. Pangeo prep ++

* "QGIS bounce" +
* UX issues:


### Ideas

* A JGIS medium-term roadmap

* Prep for pangeo showcase presentation (which will be immediately after the hackathon, please join if you want :smile: https://numfocus-org.zoom.us/j/83234473026?pwd=mgM3uAuru1AE1aFPlRjW2dAAAyo8IY.1)

* Annotations as a dataset / create vector data: https://github.com/geojupyter/jupytergis/issues/395

* Attribute table

* Python API enhancements: https://github.com/geojupyter/jupytergis/issues/436

* Re-implement "QGIS bounce" workflow in JGIS: https://github.com/geojupyter/jupytergis/issues/513

* Brainstorm mechanisms for reproducible analysis when moving between point-and-click and notebook environments: https://github.com/geojupyter/jupytergis/issues/436#issuecomment-2637601373

* Continue evolving a reproducible "processing toolbox" model: https://github.com/geojupyter/jupytergis/issues/519


## Share out

Think about:
What exciting things did you accomplish?
What loose ends remain?
Big questions? Big ideas?

* Buffer units:
    * https://github.com/geojupyter/jupytergis/pull/554
    * Decided that we would disallow the user to reproject (WIP - still need to update `command.ts`)
    * Added a custom form for buffering, doesn't quite work yet. We don't yet know how to get the projection from the source layer in the form context because we'd have to ask OpenLayers.
    * Matt will push in 1 hour
* Documentation for building documentation:
    * Created requirements-docs.md and will create PR draft
        * Use `docs/environment-docs.yml` instead (`micromamba env create -f docs/environment-docs.yml`)
    * Discussed one-click docs build -- for later! For now, let's just document the process.
    * Yao-Ting will push later today!
* Martin opened PR for disabling identify tool: https://github.com/geojupyter/jupytergis/pull/553
