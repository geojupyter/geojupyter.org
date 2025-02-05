---
title: "GeoJupyter virtual hackathon 2025-02-05"
description: |
  The first GeoJupyter virtual hackathon. Open to all!
date: "2025-02-05"
author:
  - name: "The GeoJupyter community"
categories:
  - "Hackathons"
tags: [hackathons]
---

# GeoJupyter virtual hackathon 2025-02-05

Please add new agenda items under the `New agenda items` heading!

- [Join us on Zoom](https://berkeley.zoom.us/j/92451699568)
  - [What time is the meeting in my time zone?](https://dateful.com/convert/utc?t=3pm)
- [Previous hackathons](https://geojupyter.org/blog/#category=Hackathons)
- [GeoJupyter](https://geojupyter.org) handy links:
  - [GitHub org](https://github.com/geojupyter)
  - [Community calendar](https://geojupyter.org/calendar.html)
  - [Zulip chat](https://jupyter.zulipchat.com/#narrow/channel/471314-geojupyter)


## Attendees

Your name / GitHub ID / affiliation / favorite drink this time of year

* Sanjay Bhangar / batpad / Development Seed / Chai
* Kristin Davis / kpdavi / Schmidt Center for Data Science & Environment, UC Berkeley / mint hot cocoa
* Matt Fisher / mfisher87 / DSE / Mint hot cocoa
* Yao-Ting Yao/ YaoTingYao/ Clark CGA/Mint Tea
* Martin Renou / martinRenou / QuantStack / Coffee
* Greg Mooney / gjmooney / QuantStack / Pumpkin spice latte if I'm feeling fancy
* Arjun Verma / arjxn-py / QuantStack / Cold Coffee
* Brookie Guzder-Williams/ brookisme / Coffee
* Qiusheng Wu / giswqs / University of Tennessee / Tea



## Agenda & notes

### ⚡ (5 minutes) Lightning intros

Tell us about you in 30 seconds or less!


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

**Lobby**: Orientation! Help setting up dev environment, etc. Docs: https://jupytergis.readthedocs.io/en/latest/contributor_guide/index.html
* Kristin

1. Dockerize! (https://github.com/geojupyter/jupytergis/issues/267)
    * Matt & Sanjay
    * https://github.com/geojupyter/jupytergis-docker
    * Martin: Could a GHA bot run every day and check for a new release? Should it work like the conda forge bot where it opens a PR, we review, and merge. Or just have the bot commit and tag? (the latter seems preferred)
        * Arjun: Put dockerfile in JGIS repository in `scripts/` directory?
        *
2. Python API improvements (https://github.com/geojupyter/jupytergis/issues/436)
    * Brookie & Martin & Arjun & Yao-Ting
    * Walked through workflows.
      Brookie will clean up notes and put on GitHub as a comment to the issue: https://github.com/geojupyter/jupytergis/issues/436
      Also start a chat on Zulip!

#### More

3. Layer show/hide button gets pushed off the panel (https://github.com/geojupyter/jupytergis/issues/244)
4. Improve layer gallery contributor experience (https://github.com/geojupyter/jupytergis/issues/277)
    * Martin: The gallery is generated from xyzservices Python package. How's the contributor experience for this package?
    * https://github.com/geojupyter/jupytergis/blob/b5cdceb81d316efe9dd520671a626cc533108e7f/packages/base/rasterlayer_gallery_generator.py#L9


## Share out

Think about:
What exciting things did you accomplish?
What loose ends remain?
Big questions? Big ideas?

* Share out
* Share out
* Share out


## Notes

* Brookie: `object = doc.get_feature(layer=..., feature_id=...)` to grab a unique feature out of a layer or `object = doc.get_selected_features()`
    * Sanjay: We wanted this on lonboard. Ipyleaflet has this maybe? Ability to draw a bounding box or shape, then `doc.get_bbox()` or `doc.get_features_in_bbox()`.
    * Brookie:
* Brookie: Sort collaborators alphabetically
*
