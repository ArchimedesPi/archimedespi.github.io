---
layout: post
title: writing slack bots for fun and profit
---

#### the problems
last year my robotics team had an annoying thing we had to do! so we automated it.
in the particular competition we were in, we had to submit an engineering notebook, and our internal specs for doing so said that:
- each meeting should get a section in the notebook,
  - with where we held the meeting,
  - and at what date.
- inside each meeting section there should be an announcements section holding all the announcements people had for that meeting, to make it easier to remember things we had to talk about.

this was *really* annoying to maintain. since we use slack, i thought it might be fun to make a slackbot to do this, and that's how our meeting-bot [espresso](https://github.com/ratchetrobotics/espresso) was born.


#### the solution
our notebook was a word document stored in drive. at the start of the project, i shopped around a bit for docx parsers/writers libraries, and found [python-docx](https://python-docx.readthedocs.org/en/latest/) (of course there are other docx libraries out there, but they're mostly for weird shit i don't use like .net or java). so now i had to write a slackbot in python! cool.

i took a look around for python slack clients, and came up with [python-slackclient](https://github.com/slackhq/python-slackclient) (actually written/maintained by slack themselves - thanks!) and took a quick look at [their example project](https://github.com/slackhq/python-rtmbot/) to figure out how to use it (it doesn't really have any other docs).

i got a basic example up and running and then decided i was going to overcomplicate the hell out of this thing. i wanted a plugin system so i ended up building a system to dynamically load modules using `imp.load_module`. each plugin is written with decorators specifing stimuli to respond to and then the function they're on handles the stimulus. why? because i <3 decorators: they're beautiful, easy to design, and provide an amazing api (look at flask!).
Here's a basic example of a plugin:

```python
from espresso.main import robot

@robot.respond(r"(?i)PING")
def ping(res):
    res.send("PONG")
```

with that particular yak shaved, i wrote a plugin to pull announcements in the format "Announcement for MM/DD/YY: \<announcement\>" from an #announcements channel in Slack.

#### getting people to actually use it
