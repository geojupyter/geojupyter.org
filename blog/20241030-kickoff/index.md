---
title: "Kickoff meeting"
date: "2024-10-30"
author:
  - name: "Matt Fisher"
    orcid: "0000-0003-3260-5445"
categories:
  - "Meeting notes"
---

The first meeting for the GeoJupyter project.


## Participants

* [Carl Boettiger](https://github.com/cboettig)
* [Fernando Pérez](https://github.com/fperez)
* [Ciera Martinez](https://github.com/iamciera)
* [Kevin Koy](https://github.com/kevkoy)
* [Matt Fisher](https://github.com/mfisher87)


## Values

We brainstormed our values - not in priority order.


### Computational

* Collaboration
* Cloud-native data
* ML/AI friendly
* Reproducibility (scripting)
* Client-side computing
  * Binder -> JupyterLite?
  * DEMOCRATIZING!
  * See Capytale - high school teachers created the first WASM Jupyter. Serves 500k
    French high school students per year on two computers because everything is done
    client-side.
* Distributed computing


### Artistic / learning / playing / experiential

* Creativity and exploration
* Visuals, storytelling, beauty (in exploration AND sharing/publishing)
  * Persistent view of the map! Shouldn't have to scroll up and down the notebook to see
    the cool stuff!
  * Maps & the stories they tell
* Playfulness


## Social / community considerations

* Recent challenge: How to invite new people into our Slack?
  * If we want to postpone a decision, we can just pay for those extra folks.
  * Problem remains. We need a long-term solution for the community.
* Some communities are saying "Screw it, we'll use Discord"
  * It's proprietary!
  * Conda-Forge and Apache Arrow on Zulip now.
* Short-term plan?
  * Create `#dse-geojupyter` on DSE Slack for DSE employees working on GeoJupyter
    * The `#jupyter-gis` channel can be more independent and free to address its needs
  * We can adopt something in the short-term without worrying too much.
    * Once we don't fit there anymore, because we've generated enough interest, we need to
      figure out how to scale communication!
    * The whole Jupyter project has a non-ideal communication setup. That's not going to
      be solved in two weeks.
    * Being adopted by the Linux Foundation. Fernando stepping down from exec. council.
    * Maybe next year, Jupyter is ready to choose and we jump on whatever they have
      switched to.
* How do we engage with the open source geospatial community?
  * Large community.
  * Be mindful, careful, of how we enter/interact with that community (we're
    "parachuting" in with new ideas)
  * We want to make people happy and excited to work with us!
  * Identify our first users and serve them. Interview our community, with GIF's help.
  * Framing: "We had a problem in our community, and we came up with this solution."


## Getting started ideas

* Set up interviews!
* Work with Geospatial Innovation Facility to develop use cases to guide the development
  of the tool!
* Quick-and-dirty taxonomy of existing open source tools. What are the toys in the
  toybox? Make some opinionated choices on our starting place.
* **Want to have something to show at EGU Vienna in May 2025**. AGU 2025, Fernando wants
  to be able to make noise (proposal in Spring for a Sunday workshop).
* .github repo for landing page.
* People want synchronous chat.
  * Slack / Discord / ?
* Decision record space!
* GitHub Discussions: Slower paced, Jupyter settled on Issues and PRs.
  discourse.jupyter.org is the main other place. Chris Holdgraf is currently admin, but
  Fernando isn't. Will create a new geojupyter category in discourse!
* Create a GeoJupyter website!
* Dig into JupyterGIS codebase.
* DEADLINE: In 2 months, Fernando wants to know how I think JupyterGIS fits in
  GeoJupyter.
  * Talk w/ Anne Fouilloux with Simula - responsible for jupyterGIS user stories
* DEADLINE: 15th January; abstracts due for EGU!
  https://www.egu.eu/news/1165/call-for-abstracts-to-the-egu25-general-assembly-now-open/
  * Should have something ready to show in March.
* DEADLINE: Spring 2025; submit AGU Sunday workshop abstract.
* DEADLINE: Spring 2025; propose AGU GeoJupyter session
* Before EGU: Spring 2025; working meeting in Boulder, CO?
* October 30th 2025: Funding proposal!
  * Fernando meeting with NSF Monday to pitch the idea for funding. No pressure on Matt
    for this at the moment!
* Half hour check-in every two weeks!
* Another important community: _CryoCloud_! Work there! Share prototypes, get input!
  * Prioritize Openscapes and CryoCloud
* 2i2c serves other NASA communities, they can help liaise
* Eat our own dogfood ASAP!


### Tips for getting started

* *Sacrificial concepts*
  * Sketch prototyping - draw a picture of the thing to drive iteration. Use real data!
    Real data enables people to better picture themselves using or analyzing the
    interface.
* Kevin's advice: Start simple and analog!
* Blank slate. The less we imitate existing products, the better.
  * Our architectural constraints and advantages are very different from existing
    products.
  * Don't want to be painted into a box by legacy decisions.
* AI-readiness
  * Stephan Hoyer, Berkeley grad; now at Google. Gave a talk called "Neural CGM". Machine
    learning powered short- and medium-range weather model. Making inroads in the
    context of climate predictions. Weather and climate models can be "nasty" code.
    E.g. UCAR's ESM is 40-50 years old, million lines of Fortran, large maint. team.
    * Considering feeding this huge codebase into an LLM to translate it from Fortran to
      modern Python.
    * Neural CGM runs 100k - 1million times faster than the European weather model, which
      runs on thousand+ CPUs and takes a month.
    * Hard parts are offloaded to ML trained by decades of ERA5 data.
* Inspired by this ^, we're dealing with older tools like QGIS developed in a different
  era. We have the chance to develop something new in the modern context.
  * Kevin: LLMs can help with geography rather than GIS. "Could you use LLMs to digest
    geographic thought and theory before writing our own software to do it?"


## Misc

* In our space, the output is almost always a map. Unlike Notebooks, where the output is
  more free-form / general
* [Jupyter: Thinking and Storytelling With Code and Data](https://ieeexplore.ieee.org/document/9387490) -
  "how do we think about narrative in the context of computing in Jupyter"
  * Re-imagine the storytelling aspect; but the centerpiece of the story is the map!
  * Fernando: Read this! Talk to people!
  * See ArcGIS story maps
    * <find.wilderness.org>
* How to combine/compose existing tools like Mapbox/MapLibre, QGIS, ...?
* Kevin: The analysis part is where people feel the need to fire up QGIS.
* Brookie: Bi-directional interaction with map through code. A plugin or jupyter
  notebook cell, write code that affects the map. Attach an object to a code cell
  reference. E.g. draw a box on the map and then interact with the stuff inside the box
  in the code.
  * Fernando: Mayavi Python 3d viz library. More user-friendly API for C++ mapping tool
    <___>. Fluid interaction, e.g. select something on the map and assign it to variable
    `x`! Then you can act on `x` in your code. Map adapts when modifying `x`
  * :star: CartoDB (now called Carto) had a neat trick for styling their online maps.
    Created a CartoCSS format. You write CSS to change the color of roads, line width,
    etc.
    * How to get people who can code a little (CSS, JSON) to learn a more modern way of
      working without them realizing it so much.
  * Brookie: Imagining a `Map` object, instantiated. Has a bunch of autogenerated names
    that all begin with `_`. If you change one of those autogenerated names, e.g. to
    `"restaurants"`, you can do `map.restaurants`.
    * Like Kevin's hack of reusing existing syntax
    * Andrew Bray: Deep in Quarto ecosystem, also cares deeply about storytelling.
      Showed Fernando some "scrollytelling" articles from NYT. Andrew is working on how
      to do that in Quarto!
    * Ed Tufte - Yale prof written classic books on data viz. One of his examples is
      Menard's diagram on Napoleon's march on Moscow. Andrew contacted Tufte to make a
      scrollytelling version of this map. Dynamically shows the same data over time.
* AGU got funding from Sloan in 2023 for Notebooks Now. To bring notebooks into the AGU
  peer review publication process. Funding finished, but project incomplete.
  * Involves adding to MyST authoring pipeline.
  * Fernando very interested in seeing this.
  * Wants Jupyter as part of the official scientific record for publishing. Standard
    process.
  * Audited MyST/AGU work for openness. Carthic(?). CurveNote. Hope Carthic will provide
    more funding. (Sorry, this isn't clear because I got behind on notetaking!)
  * AGU & physics communities leading the way.
  * Want scrollytelling in MyST!
