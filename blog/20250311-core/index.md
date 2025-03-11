---
title: "GeoJupyter core community meeting 2025-03-11"
description: |
  A monthly gathering of the GeoJupyter core community. Open to all!
date: "2025-03-11"
author:
  - name: "The GeoJupyter community"
categories:
  - "Meeting notes"
tags: [meeting-notes]
---

# GeoJupyter core community meeting 2025-03-11

Please add new agenda items under the `New agenda items` heading!

- [Join us on Zoom](https://berkeley.zoom.us/j/99659397059?pwd=519zZJlcAa1TCyJWRYyYbaYDfuaXNo.1)
  - [What time is the meeting in my time zone?](https://dateful.com/convert/utc?t=4pm)
- [Previous meetings](https://geojupyter.org/blog/#category=Meeting%20notes)
- [GeoJupyter](https://geojupyter.org) handy links:
  - [GitHub org](https://github.com/geojupyter)
  - [Community calendar](https://geojupyter.org/calendar.html)
  - [Zulip chat](https://jupyter.zulipchat.com/#narrow/channel/471314-geojupyter)


## Attendees

Your name / GitHub ID / affiliation

* Arjun Verma / @arjxn-py / QuantStack
* Martin Renou / @martinRenou / QuantStack
* Matt Fisher / @mfisher87 / DSE
* Nicolas Brichet / @brichet / QuantStack
* Greg Mooney / @gjmooney / QuantStack
* Brookie / @brookisme / DSE

### Action items

- [ ] Brookie: Create issue on unit conversion in buffer feature
- [ ]
- [ ]
- [ ]


### Standing items

- [ ] :left_speech_bubble: Team communication
    - :tada: What is working well?
        - Virtual hackathons :rocket:
        -
        -
    - :wrench: Opportunities for improvement. Be nitpicky!
        -
        -
        -
- [ ] :muscle: Distributing power in the community
    - "Welcome committee"
    -
    -
    -


### Follow-up from previous meeting(s)

- [ ] Matt is behind on his action items :) Still intending to reach out about creating a space in Jupyter Discourse.
- [ ]
- [ ]
- [ ]


### New agenda items

- [ ] :computer: Virtual hackathons: continue to be successful at bringing in new community members and focusing energy.
    - :hammer_and_wrench: Big topic of discussion right now: [Reproducible processing toolbox](https://github.com/geojupyter/jupytergis/issues/519)!
    -
    -
- [ ] :money_mouth_face: Looking for funding opportunities! What are you aware of?
    - NSF GEO OSE Track 2, due November. High effort.
    -
    -
- [ ] :wrench: Processing toolbox
    - Export to shapefile?
        - http://switchfromshapefile.org/
        - Brookie: Shapefiles ubiquitous. It might be a mistake not to support them!
        - We could deprioritize shapefiles?
        - Could point to an online converter tool until we support shapefile export
    - POC has been merged https://github.com/geojupyter/jupytergis/pull/510 :tada:
    - Support other units: User enters e.g. meters, convert to degrees, pass to GDAL in native projection units.
        - Spatialite supports unit conversion, but doesn't seem to be geospatially aware: <https://www.gaia-gis.it/gaia-sins/spatialite-sql-5.1.0.html#length_cvt>
        - <https://stackoverflow.com/questions/62514871/how-to-change-buffer-size-from-degrees-to-distance-by-meters-in-postgis>
- [ ] Layer export: <https://github.com/geojupyter/jupytergis/pull/528>
    - Warn users when converting vector data to raster (lossy). Hover-over :warning: icon?
    - Move format-changing operation into processing toolbox and only support exporting vector as vector and raster as raster?
    -
    -


### Pushed to next meeting

- [ ]
- [ ]
- [ ]
