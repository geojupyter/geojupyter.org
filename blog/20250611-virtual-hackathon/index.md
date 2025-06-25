---
title: "GeoJupyter virtual hackathon 2025-06-11"
description: |
  A GeoJupyter virtual hackathon. Open to all!
date: "2025-06-11"
image: "/assets/images/hackathon.jpg"
author:
  - name: "The GeoJupyter community"
categories:
  - "Hackathons"
tags: [hackathons]
---

# GeoJupyter virtual hackathon 2025-06-11

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

* Name / GitHub ID / affiliation / ?
* Yao-Ting / @YaoTingYao / ClarkCGA
* Kristin Davis / @kpdavi / Schmidt DSE
* Martin Renou / @martinRenou / QuantStack / ?????
* Matt Fisher / @mfisher87 / Schmidt DSE
* Arjun Verma / @arjxn-py / QuantStack


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

* Symbology!
    * Merge: https://github.com/geojupyter/jupytergis/pull/714
        * Ultimately the schema may need to change to have better functionality for coordinated changes to color and radius in the symbology
    * Next steps (for subsequent pull requests):
        * Remove "Fill color" option when "Graduated" is selected for "Render type"
        * Automatically re-run classify based on the field values that impact the classification. Classify depends on the selected number of classes, mode equal interval, and color ramp. Any time you change those fields, the classification could automatically update.
            * But, currently you can override classification colors. Auto-updating would remove that functionality.
            * Want to keep the "Classify" button
            * Could automatically update the classification colors when the color ramp is changed (i.e., without having to click "Classify" again)
    * The "draw features" PR (https://github.com/geojupyter/jupytergis/pull/692) may need to be restricted to just one feature type, points, lines, or polygons. How does QGIS handle GeoJSONs that have mixed geometry types?

* Documentation: Kristin to populate :smile:
    * https://github.com/geojupyter/jupytergis/issues/580


### 🪄 (all the minutes) Hack together!

Form teams from the ideas generated in the step above!


### 💬 (10 minutes) Share out

Think about:
What exciting things did you accomplish?
What loose ends remain?
Big questions? Big ideas?

Please write for people who don’t have full context; link to related issues and documentation!

* Share out 1
* Documentation
    * Kristin worked on Issue [#580](https://github.com/geojupyter/jupytergis/issues/580) but didn't get far, had to reorient self to the documentation :blush: . Will aim to work on this during another hackathon, or if is able to work on it outside a hackathon, will assign it to self on GitHub.
* GitHub label issue(?)
    * On Kristin's Firefox, labels with spaces in them aren't being searched properly - GitHub searches `label:good first issue` instead of `label:"good first issue"`. This isn't a problem on Matt's Firefox.
