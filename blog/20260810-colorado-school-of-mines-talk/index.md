---
title: "Talk: Open Science in the age of AI? Perspectives from the Jupyter ecosystem!"
description: |
    Dr. Fernando Pérez delivered this talk as an invited speaker for the Colorado School
    of Mines Department of Geophysics Heiland Lecture Series and Climate Seminar Series
    on April 29, 2026.
date: "2026-08-10"
image: "fernando-speaking.jpg"
author:
  - name: "Matt Fisher"
    orcid: "0000-0003-3260-5445"
    affiliation:
      - name: "The Eric & Wendy Schmidt Center for Data Science & Environment, UC Berkeley"
        url: "https://dse.berkeley.edu"
  - name: "Fernando Pérez"
    orcid: "0000-0002-1725-9815"
    affiliation:
      - name: "The Eric & Wendy Schmidt Center for Data Science & Environment, UC Berkeley"
        url: "https://dse.berkeley.edu"
      - name: "Department of Statistics, UC Berkeley"
        url: "https://statistics.berkeley.edu"
categories:
  - "Presentations"
---

In April 2026, Fernando Pérez delivered a talk at the Colorado School of Mines Heiland
Lecture Series that told the story of the history of Project Jupyter and the open
science movement, overviewed the power of the Jupyter architecture, and live-demoed
four example workflows that integrate free ("open-weights") Large Language Models
(LLMs) to lower barriers to insights.

Core to this talk is the idea that many of the tools and practices we depend on today
evolved from a community-wide refusal, 25 years ago, to accept a future where computing
was dominated by proprietary products and services.
That's why you're probably writing Python instead of MATLAB today.
We may be in a similar moment today: so why are many of us begging our tech overlords
for API credits?

Instead, let's co-create a future in which our work is supported by models that we fully
control, our data doesn't need to leave our home or office, and we aren't paying rent to
do our job.

You can watch Fernando's talk on YouTube below, and **read on to learn about how we
built the demos together**.

{{< video https://www.youtube.com/watch?v=_5yuXU5salY >}}


## Dream team!

Designing for these demos involved a group gathering, both virtual and in-person in
Boulder, Colorado, to co-work on software design & development, infrastructure prep,
local model evaluation, and pushing the limits of the new v3 release of
[Jupyter AI](https://jupyter-ai.readthedocs.io/).

Over the course of our collaboration, the number of demos continuously increased until
we arrived at four demos.

![Slack conversations questioning the wisdom of four live demos and discussing last-minute fixes. Participants included [Ciera Martinez](https://orcid.org/0000-0003-4296-998X), [Sam Pottinger](https://orcid.org/0000-0002-0458-4985), [Fernando Pérez](https://orcid.org/0000-0002-1725-9815), and [Matt Fisher](https://orcid.org/0000-0003-3260-5445)](./slack-goofs.jpg)

1. Local ("open-weights") AI: Using LLMs running on Fernando’s desktop Mac Mini to
   author Jupyter Notebooks.
2. A "GeoAgent" (now known as "Geospatial LLM-Enabled Navigator (GLEN)" -- more to come
   on this!) [high seas webapp](https://high-seas.nrp-nautilus.io): An AI-enabled map
   workflow for answering questions about data on
   [federally funded infrastructure](https://nrp.ai/) using open models.
3. GeoAgent workflow in JupyterLab in the cloud: a more general-purpose cloud-based
   (using [CryoCloud](https://book.cryointhecloud.com/)) workflow for experts that can
   be customized using open models.
4. Publishing from CryoCloud to GitHub: Publish outputs created in Demo 3 using free and
   open publishing methods ([MyST Markdown](https://mystmd.org/) + GitHub Pages).

![From left to right: [Cassie Buhler](https://orcid.org/0000-0003-4157-4273), [Kristin Davis](https://orcid.org/0000-0003-1204-4687), [Matt Fisher](https://orcid.org/0000-0003-3260-5445), [Tasha Snow](https://orcid.org/0000-0001-5697-5470), [Fernando Pérez](https://orcid.org/0000-0002-1725-9815)](./in-person-collaborators.jpg)

![Virtual collaborators included: [Brian Granger](https://github.com/ellisonbg), [Min Ragan-Kelley](https://orcid.org/0000-0002-1023-7082), [Carl Boettiger](https://orcid.org/0000-0002-1642-628X)](./virtual-collaborators.jpg)
