---
title: "GeoJupyter virtual hackathon 2025-04-30"
description: |
  A GeoJupyter virtual hackathon. Open to all!
date: "2025-04-30"
image: "/assets/images/hackathon.jpg"
author:
  - name: "The GeoJupyter community"
categories:
  - "Hackathons"
tags: [hackathons]
---

# GeoJupyter virtual hackathon 2025-04-30

Please add new agenda items under the `New agenda items` heading!

- [Join us on Zoom](https://berkeley.zoom.us/j/92451699568)
  - [What time is the meeting in my time zone?](https://dateful.com/convert/utc?t=3pm)
- [Previous hackathons](https://geojupyter.org/blog/#category=Hackathons)
- [GeoJupyter](https://geojupyter.org) handy links:
  - [GitHub org](https://github.com/geojupyter)
  - [Community calendar](https://geojupyter.org/calendar.html)
  - [Zulip chat](https://jupyter.zulipchat.com/#narrow/channel/471314-geojupyter)


## Attendees

Your name / GitHub ID / affiliation / What toppings are on your ideal pizza?

* Sanjay Bhangar / @batpad / Development Seed / Pepperoni
* Arjun Verma / @arjxn-py / QuantStack / Cheese & Corn
* Kristin Davis / @kpdavi / DSE / ricotta + spinach + balsamic vinegar
* Martin Renou / @martinRenou / QuantStack / A good mozzarella


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

1. Add to / improve architecture documentation: https://github.com/geojupyter/jupytergis/pull/576. (Martin, Sanjay, Kristin)
    * Review PR
    * Keep in mind that code gets outdated quickly, and thus documentation of it can as well. Can make descriptions in the documentation more high-level so we can avoid documentation getting out-of-date quickly.
2. Remove Source Panel https://github.com/geojupyter/jupytergis/issues/435 :+1: (Martin) :+1: (Arjun) - https://github.com/geojupyter/jupytergis/pull/671
3. Simplify Symbology Panel - https://github.com/geojupyter/jupytergis/issues/469 :+1: (Arjun; Martin & Kristin joined later in the hackathon)


---
Didn't work on today:

* Make Python package builds more self-contained: https://github.com/geojupyter/jupytergis/issues/585
    i) Try implementing dev environment with `pixi`?
* Annotations as a dataset / create vector data: https://github.com/geojupyter/jupytergis/issues/395
* Continue evolving a reproducible "processing toolbox" model: https://github.com/geojupyter/jupytergis/issues/519



## Share out

Think about:
What exciting things did you accomplish?
What loose ends remain?
Big questions? Big ideas?

* Simplify Symbology Panel - https://github.com/geojupyter/jupytergis/issues/469
    * Need to keep discussing this
    * Perhaps could use a style function? See example from [OpenLayers](https://openlayers.org/en/latest/examples/geojson.html)
    * Bring Greg into the conversation
        * He has an example of a style function in `mainView.tsx`
            * The style applies to everything - doesn't look for the layer type
    * Maybe remove [SimpleSymbol.tsx](https://github.com/geojupyter/jupytergis/blob/2669fad2d0c088a9718a360b267586935a65f862/packages/base/src/dialogs/symbology/vector_layer/types/SimpleSymbol.tsx), and define all prefixes (lines 94 - 98) for all different types
    * Perhaps need to change `circle-fill-color` argument to something more generic, like `color-`, and then have a way for the software to know how to apply that to different geometry types
* Arjun removed the source panel! Still has to remove some related styles - https://github.com/geojupyter/jupytergis/pull/671
* Martin, Sanjay, Kristin worked on architecture documentation and completed a revised draft - https://github.com/geojupyter/jupytergis/pull/576
