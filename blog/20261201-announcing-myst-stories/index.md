
---
title: "Announcing MyST Stories!"
description: |
  MyST Stories is a new tool for document-driven authoring of rich and interactive
  "scrollytelling" experiences.
  With MyST Stories, you can use one platform to author manuscripts, tutorials,
  curricula, workshop materials, docs, and now stories too!
date: "2026-12-01"
image: "thumbnail.jpg"
author:
  - name: "Matt Fisher"
    orcid: "0000-0003-3260-5445"
    affiliation:
      - name: "The Eric & Wendy Schmidt Center for Data Science & Environment, UC Berkeley"
        url: "https://dse.berkeley.edu"
categories:
  - "Announcements"
---

Storytelling is a powerful, but often underappreciated, mode of science communication
(<doi:10.1073/pnas.1320645111>).

Geospatial data practitioners have a large number of options for telling stories.
Options include
[ArcGIS StoryMaps](https://www.esri.com/en-us/arcgis/products/arcgis-storymaps/overview),
[Mapbox Storytelling](https://labs.mapbox.com/storytelling/),
[Cesium Stories](https://cesium.com/blog/2020/01/28/cesium-stories/),
custom JavaScript, and [more](https://github.com/kcarini/story-scrolly-mapping).
Each of these options has one or more limitations:

* Proprietary: expensive, closed, restrictive
* Lock-in: your story can only be stored and/or served on a commercial provider's
  infrastructure
* Limited: you can only visualize using maps, or you may have a small set of
  visualization tools you can use
* Difficult to author: you need software engineering expertise, or to click around
  in an overwhelming GUI, or to work with an unfamiliar/inaccessible file format
* Closed science: the work that goes in to your story is hidden; only the final
  deliverable is visible


## How MyST Stories is different

MyST Stories have none of these limitations. <...>


## Using MyST Stories

Writing a MyST Story builds on the basics of MyST Markdown.
If you've ever used [directives](https://mystmd.org/guide/directives) or
[roles](https://mystmd.org/guide/roles) before, you're off to a great start.
Otherwise, MyST Stories look similar to experiences you may have already had authoring
Markdown for GitHub or Reddit comments, READMEs, documentation, or Quarto content.

For example:

```markdown

:::{story}
:text-location: left-panel  # A CSS ID
:text-paragraph-class: card  # A CSS class
:::

Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Donec et interdum nisi.
Fusce rutrum ornare ligula ac lacinia.
Duis bibendum nibh arcu, at porttitor erat tempor sed.
Donec consectetur faucibus interdum.
Fusce interdum mi eu tincidunt feugiat.
In metus purus.

:::{story-element-init} my-map
:location: background  # A CSS ID

// TODO: Import dependency
// TODO: Think about how the thing is placed. Often viz libraries expect an HTML element
//       to be pre-created and to be passed a selector that tells it the element it
//       lives in.
// TODO: Use a real map library, not pseudocode made up one
map = Map(/* Initialize a map with some data */)
:::

Ut purus metus, tincidunt vitae blandit sed, laoreet nec lorem.
Curabitur volutpat nisl non neque cursus dictum. Donec at interdum mauris, a cursus
lacus.
Sed nec condimentum erat, et pharetra arcu.
Suspendisse laoreet orci a ex maximus, sit amet placerat dui semper.
Integer semper augue justo, eget dapibus sapien facilisis eu.
Mauris dignissim efficitur leo, ac pulvinar purus tempor sit amet.

:::{story-trigger}
:trigger-at: middle
map.flyTo(/* Some coordinates/zoom */)
:::

Name at orci dolor.
Quisque condimentum dolor eu tristique ullamcorper.
Proin quis leo rutrum neque malesuada pharetra eget sed mi.
Curabitur ut semper tellus.
Sed nec ante quam.
Curabitur iaculis maximus risus, et dignissim massa vestibulum mattis. Duis consectetur.

:::{story-trigger}
:trigger-at: middle
map.flyTo(/* Some other place */)
:::

Tada.

:::{story-element-end} my-map
:transition: fade
:::

:::{story-element-init}
:location: right-panel  # A CSS ID

plot1 = Plot(/* Initialize a plot with some data */)
:::

:::{story-trigger}
:trigger-at: top
// ?
:::

:::{story-end}
:::
```


## Try it today!

:::{note}
This presumes a new mechanism to install MyST plugins.
:::

You can install MyST Stories with several tools:


:::{.panel-tabset}
## pip
```bash
pip install myst-stories
```

## uv
```bash
uv add myst-stories
```

## conda/mamba
```bash
mamba install myst-stories
```

## pixi
```bash
pixi add myst-stories
```
:::

Now you can write your story and use `myst build --html` to render it to a beautiful
interactive website.

Read our [quick start guide](https://example.com) for more info about getting started.
