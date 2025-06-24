---
title: "JupyterGIS sync meeting 2025-06-24"
description: |
  A weekly gathering of JupyterGIS team to discuss our progress and help each other out.
  Open to all, but this meeting is _short_ and task-focused, so there will not be time
  for introductions. Please join a core meeting!
date: "2025-06-24"
image: "/assets/images/standup.jpg"
author:
  - name: "The GeoJupyter community"
categories:
  - "JupyterGIS notes"
tags: [jupytergis-notes]
---

:::info {.callout-info}
:mag: This meeting is _short_ and _task-focused_. Unfortunately, we won't have time to
introduce every new person to the team. Please attend core community meetings ([see
GeoJupyter calendar](https://geojupyter.org/calendar)) to meet the team and add your own
agenda items, and/or
[introduce yourself on Zulip](https://jupyter.zulipchat.com/#narrow/channel/471314-geojupyter/topic/Welcome)!
:::

# JupyterGIS sync meeting 2025-06-24

Please add new agenda items under the `New agenda items` heading!

- [Join us on Google Meet](https://meet.google.com/zhk-vygf-gke)
  - [What time is the meeting in my time zone?](https://dateful.com/convert/utc?t=4pm)
- [Previous meetings](https://geojupyter.org/blog/#category=JupyterGIS%20notes)


## Attendees

Your name / GitHub ID / affiliation

* Martin Renou / @martinRenou / QuantStack
* Matt Fisher / @mfisher87 / DSE


## Agenda

* Review our [project board](https://github.com/orgs/geojupyter/projects/2)
  * What items should be added?
  * Are there stale items that are no longer urgent?
  * Are there things we can change about the project board to make it more useful? Add
    more information? Remove steps?
* _Please add more items if you have them!_


### Status reports

* STAC browser PR
    * The hardcoded API (geodes) is down, should be back in 2 days
    * Greg tested some other STAC endpoints, and some worked, some didn't
* Processing toolbox refactor by Guy
    * How to validate the JSON data? Take this on in another PR.
    * Matt to give final review today!
* Symbology overhaul:
    * No significant progress since last hackathon
    * Going to try to make progress today in preparation for hackathon tomorrow
* Draw vector features on the map:
    * Matt to review this week!
    * Should we keep this PR open until we can do the vector sub-type development? We don't want to introduce a new feature and then revoke it. This PR should be easy to rebase if the trunk changes.
* Should we have a 2nd trunk branch to help use release features more selectively?
    * Increases maintenance burden and contributor complexity
    * We don't have enough maintainers right now for this
    * We think we will probably reach a point where this is necessary as the project's scope grows.
