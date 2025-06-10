---
title: "GeoJupyter core community meeting 2025-06-11"
description: |
  A monthly gathering of the GeoJupyter core community. Open to all!
date: "2025-06-11"
image: "/assets/images/community-meeting.jpg"
author:
  - name: "The GeoJupyter community"
categories:
  - "Meeting notes"
tags: [meeting-notes]
---

# GeoJupyter core community meeting 2025-06-11

Please add new agenda items under the `New agenda items` heading!

- [Join us on Zoom](https://berkeley.zoom.us/j/99659397059?pwd=519zZJlcAa1TCyJWRYyYbaYDfuaXNo.1)
  - [What time is the meeting in my time zone?](https://dateful.com/convert/utc?t=4pm)
- [Previous meetings](https://geojupyter.org/blog/#category=Meeting%20notes)
- [GeoJupyter](https://geojupyter.org) handy links:
  - [GitHub org](https://github.com/geojupyter)
  - [Community calendar](https://geojupyter.org/calendar.html)
  - [Zulip chat](https://jupyter.zulipchat.com/#narrow/channel/471314-geojupyter)


## Attendees

Your name / GitHub ID / affiliation / what do you plan to do when taking a break today?

* Arjun Verma / @arjxn-py / QuantStack / Spend time with my niece
* Nicolas Brichet / @brichet / QuantStack / ?
* Martin Renou / @martinRenou / QuantStack / Did some tidying in the shed
* Matt Fisher / @mfisher87 / Schmidt DSE / pull some weeds in my garden! :seedling: 
* Tyler Erickson / @tylere / VorGeo / shopping at Trader Joes
* 


### Standing items

- [ ] Feedback on team communication and productivity?
    - What's going well?
        - I think the new project board is working great!
        - Everyone is awesome and helps each other out
        - 
        - 
        - 
    - Areas for improvement?
        - More diversity in contributor base
        - 
        - 
        - 


### Follow-up from previous meeting(s)

- [ ]


### New agenda items

- [x] Team compass: <https://compass.geojupyter.org/>
- [ ] Matt planning to start working on reproducible processing toolbox. 
    - Will work on Symbology rough edges first!
    - Implementation / architecture thoughts?
    - (Martin) Guy started recently, working on processing toolbox. Started adding gdal commands to the schema to help refactor the schema functions in TS to reduce the number of places a change is required to add more processing commands.
        - What about processing functions that are conditional based on the layer type?
            - Martin: Instead of disabling buttons, let's show a nice error.
                - Matt: What about simple cases like disabling based solely on layer type?
        - Matt: Planning to try and meet up with Guy and chat during the morning sometime soon.
    - Nicolas: Do the processing steps save in the shared document?
        - Martin: There's a checkbox in the dialog to either save as a separate file or to embed the data in the shared document.
- [ ] ESA Living Planet Symposium @ Vienna -- [JupyterGIS workshop](https://lps25.esa.int/programme/programme-session/?id=B97391AC-F0D6-4C3D-B38C-FB69AA1219D6)
    - Tyler: Not familiar on what will be taught yet! Helper.
    - TODO (Matt): Save the workshop under `workshops.geojupyter.org`!
- [ ] Jupyter community call tomorrow at 9AM PT. Anyone joining? Anything you want Matt to share? I have a 3 minute speaking slot.
    - Can we do a release beforehand? It'd be great, but let's not rush it :)
- [ ] Symbology panel refactor demo!


### Pushed to next meeting

- [ ]
