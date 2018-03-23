---
layout: post
title:  "Welcome to the new Warlock site!"
author: sproctor
date:   2018-03-22 10:20:28 -0400
categories: warlock update
---
I'd like to apologize for how poorly Warlock has been maintained these past 6 or 7 years. We've had a mix of declining user
interest and developers with other priorities.

When we are active, we've done a lot of work that never made it into a release. The current state of the Warlock 2 application is
much better in the github repository than the last version that was pushed over to SourceForge. You can find some newer builds
over on [our build site](http://build.warlock.cc/). Those will not be automatically updated because I never figured out how to
get the updater working when we updated Eclipse versions. Which brings me to the point of all of this...

Upgrading versions of Eclipse was extremely painful. It broke the updater and cause strange behavior in the UI. The solution to
both of those problems was to start re-architecting things. If we stayed with Eclipse, it was going to be a lot of work invested
into a platform that appears to be stagnating. The complications to the release cycle that come from building on Eclipse do not
appear to be worth what they provide when there are options now that didn't exist when we started this project. Which brings me to
the _actual_ point of this...

I've started a [complete rewrite](https://github.com/sproctor/warlock3) of Warlock 2 in Kotlin and TornadoFX/JavaFX. The UI will be
very similar to Warlock 2. This project is still in its infancy. I expect to have something worth demonstrating in a couple of
weeks.

You can view [our old posts here](https://sourceforge.net/p/warlock/news/).
