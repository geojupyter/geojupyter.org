---
title: "GeoJupyter virtual hackathon 2025-02-19"
description: |
  A GeoJupyter virtual hackathon. Open to all!
date: "2025-02-19"
image: "/assets/images/hackathon.jpg"
author:
  - name: "The GeoJupyter community"
categories:
  - "Hackathons"
tags: [hackathons]
---

# GeoJupyter virtual hackathon 2025-02-19

Please add new agenda items under the `New agenda items` heading!

- [Join us on Zoom](https://berkeley.zoom.us/j/92451699568)
  - [What time is the meeting in my time zone?](https://dateful.com/convert/utc?t=3pm)
- [Previous hackathons](https://geojupyter.org/blog/#category=Hackathons)
- [GeoJupyter](https://geojupyter.org) handy links:
  - [GitHub org](https://github.com/geojupyter)
  - [Community calendar](https://geojupyter.org/calendar.html)
  - [Zulip chat](https://jupyter.zulipchat.com/#narrow/channel/471314-geojupyter)


## Attendees

Your name / GitHub ID / affiliation / What’s your favorite way to waste time?

* Martin Renou / martinRenou / QuantStack / I don't have a favorite way to waste time, but I hate wasting time on social media
* Kristin Davis / kpdavi / Schmidt DSE / Playing Stardew Valley
* Yao-Ting Yao / YaoTingYao / ClarkCGA / Watch Youtube
* Jon Marokhovsky / @jmarokhovsky / ClarkCGA / Playing Rocket League
* Matt Fisher / @mfisher87 / Schmidt DSE / Playing with my dogs! Emulating Super Nintendo games :)



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

Join the corresponding breakout room to hack!

Helpful labels:
* Good first issue: https://github.com/geojupyter/jupytergis/issues?q=sort%3Aupdated-desc%20is%3Aissue%20is%3Aopen%20label%3A%22good%20first%20issue%22
* Hackathon: https://github.com/geojupyter/jupytergis/issues?q=sort%3Aupdated-desc%20is%3Aissue%20is%3Aopen%20label%3Ahackathon

**Lobby**: Orientation.+JM

1. Continue brainstorming Python API improvements with a focus on reproducibility (https://github.com/geojupyter/jupytergis/issues/436) +YT
2. Converting project documentation from reST to MyST (Kristin was assigned this task on GitHub =D)


### Not today

3. Consider how to implement workflows for manually & collaboratively building a vector dataset representing personal knowledge/observations (https://github.com/geojupyter/jupytergis/issues/395)


## Share out

Think about:
What exciting things did you accomplish?
What loose ends remain?
Big questions? Big ideas?

* Implemented remove layer method: https://github.com/geojupyter/jupytergis/pull/478
* A `dev container` approach to avoid issues with WSL / Windows / OSX issues - but how does this interact with the JupyterLab workflow??
    * https://github.com/microsoft/vscode-dev-containers/blob/main/script-library/docs/jupyterlab.md
* Thinking about Python API and reproducibility.
    * What about "recording" a manifest of actions taken in the GUI and generating Python code? Suggested by Nick :) How will this work? :thinking_face:
* Converted `troubleshooting.rst` to .md! [PR here](https://github.com/geojupyter/jupytergis/pull/479)
    * Will reviewers assign themselves to PRs or should PR-makers assign them before posting the PR?
* We should simplify the documentation building setup to optionally build jupyterlite
    * Could we push jupyterlite builds to an artifact registry to speed up CI/CD?
* Martin walked Jon through setting up a JupyterGIS Dev Environment and everything worked first try! :confetti_ball:
* Still a few more files to convert to MyST, but the process is straightforward with `rst2myst`
    * Kristin will (try) to convert one more doc from .rst to .md before next hackathon
* I've put QuantStack's internal git guidelines in public here <https://github.com/martinRenou/git_tutorial/blob/main/git/git_workflow.md> for those interested :raised_hands:
