---
title: "GeoJupyter virtual hackathon 2025-05-14"
description: |
  A GeoJupyter virtual hackathon. Open to all!
date: "2025-05-14"
image: "/assets/images/hackathon.jpg"
author:
  - name: "The GeoJupyter community"
categories:
  - "Hackathons"
tags: [hackathons]
---

# GeoJupyter virtual hackathon 2025-05-14

Please add new agenda items under the `New agenda items` heading!

- [Join us on Zoom](https://berkeley.zoom.us/j/92451699568)
  - [What time is the meeting in my time zone?](https://dateful.com/convert/utc?t=3pm)
- [Previous hackathons](https://geojupyter.org/blog/#category=Hackathons)
- [GeoJupyter](https://geojupyter.org) handy links:
  - [GitHub org](https://github.com/geojupyter)
  - [Community calendar](https://geojupyter.org/calendar.html)
  - [Zulip chat](https://jupyter.zulipchat.com/#narrow/channel/471314-geojupyter)


## Attendees

Your name / GitHub ID / affiliation / What are you drinking this morning/evening?

* Sanjay Bhangar / @batpad / Development Seed / Chai
* Matt Fisher / @mfisher87 / Schmidt DSE / Raspberry lemonade!
* Arjun Verma / @arjxn-py / QuantStack / Lemonade
* Kristin Davis / @kpdavi / DSE / Regular coffee (booring but works =])
* Felipe Montealegre-Mora / @felimomo / DSE / Specialty coffee from Finca Mora >:) learning how to properly pour over!
*
*
*


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

1. Symbology Panel UX Improvements:
    - https://github.com/geojupyter/jupytergis/issues/694
    - https://github.com/geojupyter/jupytergis/issues/695
3. File dialog scrunches file names (https://github.com/geojupyter/jupytergis/issues/389) ++


### Didn't work on

5. GISDocument doesn't respect `projection` argument (https://github.com/geojupyter/jupytergis/issues/688)
6. Document supported data formats (https://github.com/geojupyter/jupytergis/issues/317)
7. Document our breaking change policy (https://github.com/geojupyter/jupytergis/issues/641)
8. New demo image / animation for README (https://github.com/geojupyter/jupytergis/issues/334)
9. Enable viewing source and layer metadata (https://github.com/geojupyter/jupytergis/issues/471)



## Share out

Think about:
What exciting things did you accomplish?
What loose ends remain?
Big questions? Big ideas?

* File dialog scrunches / truncates file names
    * The file dialog comes from `@jupyterlab/filebrowser`
    * It's the same as the file browser on the left panel
        * The file browser on the left panel works perfectly!
    * We're just using in a different context to display it as a modal
        * Maybe the context is the problem, and the file browser in the left panel depends on some CSS from a parent element to look correct?
        *
    * Reproduction is inconsistent :exploding_head: :melting_face:
        * Some people/browsers see ellipses, some people don't
            * Sanjay sees ellipses in Firefox, no ellipses in Chrome
        * Some people see truncation, some people don't
            * It doesn't seem like truncation depends on the browser
        * It seems to have nothing to do with browser model or browser version
            * Matt (Ubuntu) was using Firefox 137, and it reproduced
            * Kristin (Mac) was using Firefox 138, and it did not reproduce
            * Matt upgraded to Firefox 138, and it did reproduce
            * Martin (Fedora) was using latest Firefox, and it did not reproduce
            * Sanjay (Mac) reproduced in Chrome & Firefox 137
            * Arjun (Mac) was using Chrome, unable to reproduce fully
                * Decreasing width of the file browser hides modified dates
                * But the filenames never get scrunched
            * Felipe (Mac) was using Safari & Firefox, and it reproduced
    * Fiddling around with styles sometimes helps, but hasn't yet yielded a full solution where the dialog works exactly like the file browser in the left panel.
        * TODO: Sanjay to fill out some of the things he's tried!
    * DID SANJAY ('s drunk AI companion) FIX IT ?!?!?!?!?!
        * How? ... TODO ...
            * Sanjay modified packages/base/source/style/dialog.css
                * In the main branch, there's basically nothing in that file

* Were able to fix :tada::
    * Symbology panel: color steps are not recovered properly after setting graduated radius - https://github.com/geojupyter/jupytergis/issues/694 with https://github.com/geojupyter/jupytergis/pull/700
