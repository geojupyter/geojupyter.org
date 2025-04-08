---
title: "GeoJupyter core community meeting 2025-04-08"
description: |
  A monthly gathering of the GeoJupyter core community. Open to all!
date: "2025-04-08"
author:
  - name: "The GeoJupyter community"
categories:
  - "Meeting notes"
tags: [meeting-notes]
---

# GeoJupyter core community meeting 2025-04-08

Please add new agenda items under the `New agenda items` heading!

- [Join us on Zoom](https://berkeley.zoom.us/j/99659397059?pwd=519zZJlcAa1TCyJWRYyYbaYDfuaXNo.1)
  - [What time is the meeting in my time zone?](https://dateful.com/convert/utc?t=4pm)
- [Previous meetings](https://geojupyter.org/blog/#category=Meeting%20notes)
- [GeoJupyter](https://geojupyter.org) handy links:
  - [GitHub org](https://github.com/geojupyter)
  - [Community calendar](https://geojupyter.org/calendar.html)
  - [Zulip chat](https://jupyter.zulipchat.com/#narrow/channel/471314-geojupyter)


## Attendees

Your name / GitHub ID / affiliation / favorite flavor of ice cream (or other dessert)?

* Nicolas Brichet / @brichet / QuantStack / ?
* Fernando / GitHub ID / affiliation / ?
* Matt Fisher / @mfisher87 / DSE / adzuki bean (red bean)
* Greg Mooney / @gjmooney / QuantStack / Cookie Dough



### Standing items

- [ ] :left_speech_bubble: Team communication
  - :tada: What is working well?
    - Virtual hackathons, of course :wink:
    - ?
    - ?
  - :bulb: Opportunities for improvement?
    - More virtual hackathon timeslots? What timing would enable you to participate in the hackathon?
    - Building more energy in Zulip channel.
    - Building up a larger contributor base.
    - ?
    - ?


### Follow-up from previous meeting(s)

- [ ] Follow-up here
- [ ] Matt: Contact Jupyter folks about creating a GeoJupyter space in the Jupyter Discourse


### New agenda items

- [ ] AGU2025
  - Planning on a session and a workshop
  - Session: Full day, posters in morning, oral in afternoon.
  - Workshop: 3.5 hours or 7 hours. Not GeoJupyter specific; open source and cloud native tools.
- EGU in May 2025, anyone in QuantStack going? **Ask in Zulip.**
- [ ] GeoJupyter Focus Group @ Berkeley campus
  - Super productive!
  - Insights:
    - :x: "No metadata" still very common problem.
      - We can make our interface more usable than QGIS', take inspiration from epsg.io for example.
    - :confounded: Too many data formats!
      - :sob: "I feel despair when opening a NetCDF"
    - :left_speech_bubble: "I want my actions in an interface to produce a script to be reproducible."
    - :video_game: I want to do it multiplayer.
    - :sparkles: "Too much prep work before I can even visualize my input data."
    - :chart_with_upwards_trend: Lots of R users.
      - :medal: "My favorite tool is R|ggplot|GEE|StoryMaps"
- [ ] Progress on a new dance called :dancer: "The JupyterGIS bounce" :dancer:
  - :heart: Awesome work Arjun, Martin, Nicolas!
  - Would love your review on WIP [blog post](https://github.com/geojupyter/geojupyter.org/pull/64)
  - PRs:
    - :wrench: [WIP: Add new function `geo_debug(my_data)`](https://github.com/geojupyter/jupytergis/pull/340) - opens a JGIS panel (new document) to explore `my_data` (including a basemap).
      - Better name for this function? Proposed:
        - `show()` - could be confused with other `show()` functions which open a widget to simply display an object; this function will create a new document and pre-populate it with a layer
        - Nicolas: `sandbox()` `playground()`
        - Fernando: `geo_explore()`, `explore()`
      - Update path for widget:
          - Filepath passed to model is only informative.
          - sharedModel, not model, is the thing that shares data with the server.
          - No way to update the file target, it's a read-only property.
          - Better to create a new widget and replace.
          - Nicolas: Maybe we shouldn't do this; re-running the notebook would replace the widget again
          - Fernando: It's important that certain patterns of behavior are consistent across Jupyter components. Notebooks are documents, consoles are throwaway environments. Notebooks always live on disk, but if not named have a name slug.
            - Nicolas: What about a file naming convention to indicate that this is a temporary file?
            - Fernando: Untitled1.jGIS!
    - :wrench: [WIP: Add "Save as..." to UI](https://github.com/geojupyter/jupytergis/issues/594)
    - :heavy_check_mark: [Add "Save as..." to Python API](https://github.com/geojupyter/jupytergis/issues/593)
    - :heavy_check_mark: [Display toolbar in widget/sidecar views](https://github.com/geojupyter/jupytergis/issues/397)
- [ ] GeoJupyter architecture documentation and contributor tutorials
  - :heart: Awesome work Sanjay, Arjun, Martin!
  - :index_pointing_at_the_viewer: Could use your help!
  - [Architecture docs first draft](https://github.com/geojupyter/jupytergis/pull/576)
  - [Contributor tutorial - add keybindings](https://github.com/geojupyter/jupytergis/pull/586)
  - In progress contributor tutorial - add new command (no PR yet)
  -
  - /

### Pushed to next meeting

- [ ]
