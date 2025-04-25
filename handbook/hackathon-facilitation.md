---
title: "⌨️ Hackathon facilitation guide"
---

## Prereqs

### Ensure you have host permissions on the hackathon meeting

Join the hackathon meeting Zoom and check that you can create breakout rooms.


## Create hackathon meeting notes ahead of time

Try to do this the Monday before the hackathon, or earlier.


### Run the automation

Navigate to the [GitHub Actions workflow for creating and syncing meeting
notes](https://github.com/geojupyter/geojupyter.org/actions/workflows/meeting-notes.yml):

* Click "Actions" at the top navigation bar of the
  [geojupyter.org repository](https://github.com/geojupyter/geojupyter.org).
* On the left, select "Setup / sync meeting notes".
* On the upper-right, click "Run workflow".
    * Keep the "Branch" dropdown set to "main".
    * Select "virtual-hackathon" as the meeting type.
    * Enter the meeting date, e.g. "this wednesday" or "2025-04-30".
* Click "Run workflow".


This will create a new document in HackMD under the
[GeoJupyter project](https://hackmd.io/@geojupyter) as well as a
[pull request](https://github.com/geojupyter/geojupyter.org/pulls).


### Grant edit permission to "everyone" in HackMD

* Navigate to the new document in HackMD, which will be linked from the new pull request.
* Click "Edit" in the upper right.
* Click "Share" in the upper right.
* Set "Write" permission to "Everyone".
* The setting is immediately saved!


### Pre-populate some hackathon activities

Under the "Hack Teams" section of the doc, replace the numbered list with placeholder
text reading "Objective" with some hackathon ideas. You can reuse ideas from previous
hackathons that didn't get completed, or if you're not sure you can ask for help from
hackathon participants to populate the list.

If you're unsure ahead of the hackathon, reach out to Martin Renou or Sanjay Bhangar on
Zulip to ask for help!

**Hackathon activities do not have to be coding activities**: You can work on
documentation or brainstorming features or API design.


## Announce the hackathon in Zulip

In the
[Zulip #geojupyter channel](https://jupyter.zulipchat.com/#narrow/channel/471314-geojupyter),
announce the hackathon by creating a new topic with the title `Hackathon YYYY-MM-DD`.
Look at previous hackathon announcements for inspiration!

* Share the link to the hackathon notes.
* Include a link to the [community calendar](https://geojupyter.org/calendar).
* Include hackathon activity ideas from the notes document.
* Encourage attendees to add their ideas to the notes document ahead of time.


## Meeting facilitation

### Admit people from the waiting room

Keep an eye on the Zoom meeting (you may want to keep it visible on a secondary display)
for joiners and admit them as they come.


### Meeting flow

Follow the document, starting with the "Agenda & notes" section.
The general flow of the meeting is outlined there.

Unless everyone there knows each other already, we start with lightning introductions.
**It's important to emphasize what we mean by "lightning" -- 30 seconds or less, say
your name, your affiliation, and your role.**

When someone has something to demo, we can take 5 minutes after introductions for the
demo, but again, reinforce that demos should be quick and leave time for hacking.

Team forming is the last step before hacking.
We take around 5 minutes, sometimes more, to decide what we want to work on together.
Encourage people to add their ideas to the "Hack teams" section of the document.
Encourage people to note their interest in ideas with a `+` at the end of the line.

Identify a reasonable number of activities for the group that attends, for example if
there are 5 attendees, propose 2 activities.

Create breakout rooms for the teams.
Always create some extra breakout rooms in case someone wants to work quietly!

The bulk of the time from this point is for hacking.


### Hacking

Encourage less experienced folks to be "drivers" (typing and screensharing) and more
experienced folks to be "navigators" (helping instruct the drivers).

Encourage rotation of roles!

It may help to use VSCode LiveShare for this: The driver can create a LiveShare session
and share the link with the group, who can join and collaborate with the driver.
This also enables the driver to
[share their JupyterLab server](https://learn.microsoft.com/en-us/visualstudio/liveshare/use/share-server-visual-studio-code#share-a-server)
so that collaborators can interact with the deployed service.

Explore a problem together!
Remind folks that it's OK not to know the answer, that's what hackathons are for :smile:
