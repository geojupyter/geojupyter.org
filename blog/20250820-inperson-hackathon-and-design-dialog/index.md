---
title: "In-person Hackathon and Design Dialog 2025"
description: |
  On August 13-14 in Berkeley CA, a group of ~25 dedicated geospatial professionals had a
  meeting of the minds. We worked together on code, design, and big-picture strategy!
date: "2025-08-20"
image: "group-photo.jpg"
author:
  - name: "GeoJupyter Hackathon participants (see below)"
categories:
  - "Events"
---

When 25 geospatial professionals gathered in Berkeley for a
[2-day intensive hackathon event](https://events.geojupyter.org/hackathons/202508-berkeley/),
we didn't just write code, we reimagined what JupyterGIS could become.


![A group photo of the in-person hackathon participants](group-photo.jpg){.lightbox}


:rainbow: With backgrounds and skills all over the spectrum, everyone had something to teach and
something to learn, creating a multiplier effect where our diversity amplified
each other's contributions.

Four distinct working groups quickly emerged:

* infrastructure developers exploring containers and development environment setup,
* documentation specialists filling in gaps and testing tutorials with fresh eyes,
* API developers working on Python integration and data manipulation workflows, and
* strategists zooming out to question JupyterGIS' fundamental purpose.

Each team made valuable contributions and wrote a summary of their activities:


## :building_construction: Development infrastructure team

* Worked together to set up development environments for the first time
* Explored using devcontainers to reduce startup burden for new contributors

  > This is an interoperable development container that automates the dev environment
  > setup for JupyterGIS development.
  > It works both on Hub infrastructure and on VSCode / Codespaces without any
  > additional tinkering!
  > This means that users, regardless of their host OS, can build and iterate on
  > JupyterGIS either locally (using Docker or Docker + VSCode) or in the cloud (on
  > managed Hub infrastructure or GitHub codespaces).
  > A byproduct of this work was the development of a
  > [Dev Container Feature](https://github.com/GondekNP/devcontainer_jupyterhub_interoperator)
  > that provides a way for Jupyter-based images to play nice with `devcontainer`-based
  > tools without fuss, something I have been annoyed with for some time.

* Discussed the potential of using a JupyterHub for developing on JupyterLab extensions


## :books: Documentation team

> Our hackathon topic brought together a diverse set of backgrounds and personas of
> potential JupyterGIS users to test out and improve existing documentation and
> tutorials.
> Several pull requests, bug reports and feature suggestions were created and the
> JupyterGIS project gained another 9 testers.
> Repeating this experiment by giving this task to different types of user working
> groups is one great way to help build a roadmap and envision the future of this
> project.

* Tested JupyterGIS and reported bugs
  ([#869](https://github.com/geojupyter/jupytergis/issues/869))
* Suggested new features
  ([#871](https://github.com/geojupyter/jupytergis/issues/871),
  [#876](https://github.com/geojupyter/jupytergis/issues/876))
* Updated the structure of the JupyterGIS examples with a "guided tour" feel
  ([#872](https://github.com/geojupyter/jupytergis/pull/872),
  [#878](https://github.com/geojupyter/jupytergis/pull/878)
  [#875](https://github.com/geojupyter/jupytergis/issues/875))
* Tested JupyterGIS tutorials for accuracy and clarity, and submitted fixes
  ([#873](https://github.com/geojupyter/jupytergis/pull/873))
* Reviewed documentation prose and inline documentation (like docstrings) for clarity
  and errors, and submitted fixes!
  ([#874](https://github.com/geojupyter/jupytergis/pull/874),
  [#867](https://github.com/geojupyter/jupytergis/pull/867),
  [#868](https://github.com/geojupyter/jupytergis/pull/868),
  [#873](https://github.com/geojupyter/jupytergis/pull/873),
  [#864](https://github.com/geojupyter/jupytergis/pull/864))


## :snake: Python API ergonomics team

> We worked on getting data out of the map layer, manipulating the data and making
> updates to the map.
> We showed this was possible through two different workflows: toggling layer visibility
> and getting GeoJSON from the layer source and turning it into a geopandas object.

Please see [#877](https://github.com/geojupyter/jupytergis/pull/877) for this team's
prototype!


## :world_map: Strategy team

> We followed a detailed user story focused on biodiversity and identified some gaps and
> opportunities.
> We thought about what problems JupyterGIS should and should not try to solve and
> identified overlap with things Notebooks are good at and many researchers are
> comfortable doing in Notebooks -- analysis.
> By focusing more on visualization, an area where many practitioners already struggle
> and a reason they open QGIS, we feel we can more quickly deliver a product that can be
> used in daily work.
> We also identified a robust STAC search implementation and GUI as something
> alternatives do not excel at, and a possible "killer feature".


* What should JupyterGIS be? What should JupyterGIS _not be_?
    * Should focus on the areas where users need the most help.
      For example, visual exploration is the most broadly-reported challenge.
    * Should not focus on drawing users away from Jupyter Notebook analysis workflows
      that are working for them and are well-served by Notebooks.
      For example, providing utilities in the visual environment that serve Notebook
      workflows: drawing or calculating areas of interest and moving those back over to
      the Notebook, synchronizing changes in Python data objects over to the map.
      **Not** trying to reimplement the QGIS/ArcGIS model builders unless we have a
      strong value-add.

    ![A Venn diagram illustrating overlap with Jupyter Notebooks](jupytergis-notebook-venn.jpg)

* Why do people leave QGIS?
    * Scaling analyses or performing analysis on big datasets
    * Repeatability & reproducibility with a Notebook or script
* Why do people come back to QGIS?
    * Exploring results
    * Making a map to share or tell a story


## :heart: Thank you :bow:

Thank you _so much_ to our wonderful hackathon participants for bringing a collaborative
energy and creating a supportive atmosphere that made it fun and safe to take on hard
problems!

Infinite thanks to our fantastic team of facilitators from
[Berkeley Institute for Data Science (BIDS)](https://bids.berkeley.edu) and
[Schmidt Center for Data Science and Environment (DSE)](https://dse.berkeley.edu)
who curated equipment and a comfortable environment, solved problems, provided delicious
caffeine and meals, expertly facilitated discussions, and more.

Finally, thanks to [Berkeley Institute for Data Science
(BIDS)](https://bids.berkeley.edu) for hosting us at their wonderful
[AI Futures Lab](https://bids.berkeley.edu/news/announcing-ai-futures-lab-visionary-partnership-between-bids-and-uc-investments)
space on day 1!
What a view :star_struck: :bridge_at_night:


## :mega: Call to join the community

We want to work with :index_pointing_at_the_viewer: **you**!
With your collaboration, we can build less frustrating and more joyful and rewarding
ways of working with geospatial data.
Here's how:

:open_book: [Share a story about a workflow that needs improvement](https://github.com/geojupyter/jupytergis/issues/new?template=0-user-story.yml)!

:calendar: [Join a hackathon or community meeting](https://geojupyter.org/calendar)!

:left_speech_bubble: [Chat with us on Zulip](https://jupyter.zulipchat.com/#narrow/channel/471314-geojupyter)!

:test_tube: [Try JupyterGIS](https://jupytergis.readthedocs.io/)! Where does it (not)
meet your needs?

:sunglasses: Share your rad vibes and leadership!

:love_letter: Get in touch with our community manager:
[Zulip](https://jupyter.zulipchat.com/#narrow/channel/471314-geojupyter),
[GitHub](https://github.com/mfisher87), [email](mailto:matt.fisher@berkeley.edu)


---

_This post co-created by hackathon participants:
  Arjun Verma,
  Brianna Pagan,
  Brookie Guzder-Williams,
  Ciera Martinez,
  Fernando Pérez,
  James Colliander,
  Jason Grout,
  Jon Atkins,
  Kevin Koy,
  Kirstie Whitaker,
  Kristin Davis,
  Lucia Layritz,
  Maryam Hosseini,
  Maryam Vareth,
  Matt Fisher,
  Maxwell Taniguchi-King,
  Maya Weltman-Fahs,
  Maya Zomer,
  Michele Tobias,
  Min RK,
  Nick Gondek,
  Qiusheng Wu,
  Shane Grigsby,
  Stace Maples,
  Tyler Marino_
