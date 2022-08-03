---
layout: post
title: "Warlock 3 reaches beta"
author: sproctor
date: 2022-07-06 16:38:00 -0400
categories: warlock update
---
Warlock 3 beta03 is out now for testing. There are builds for Windows, Mac, and Linux. The big missing items mentioned in the last post are all implemented.

I promised script improvements, and I've delivered. You can check the docs for porting Warlock 2 scripts. The same process will mostly apply to Genie scripts if you're interested in converting them. A couple of notes about variables: Warlock 2 had a bit of a weirdness with global/local variables. We had copied Genies usage of "$" to mark a different type of variable, except with the reverse usage as them. When I wrote the script engine, I was more familiar with Wizard scripts and I hadn't used StormFront much. Warlock 3 gets this more correct, but please let me know if you have any issues. The "$" variable indicator has been dropped. All variables now share the same namespace. There are 3 types of variables: client variables that are stored in settings and can be used in multiple scripts, script global variables that will shadow a client variable if used, but aren't persisted, and local variables that will shadow any other variable and are only scoped to the current function.

I've implemented an escape mechanism using %{}. Anything inside the braces will be treated as a special expression and parsed using a bit more formal parser than is typical in scripts. Variables can be prefixed with % there, but it's not manditory. For the moment, it's the only way to access properties of maps: ie. "%{properties["health"]}". 

All preferences are now stored in a sqlite DB at %HOME/.warlock3/prefs.db. You can copy that file to back it up and overwrite it with the backup if something goes wrong with your settings. I'm planning to implement import/export functionality, but it's not high on my list of priorities.

The biggest improvement in beta02 is the introduction of the dashboard. You can now quickly connect to any previously connected character. beta03 brings the ability to reconnect without restarting the client, and connect through Lich. Lich 5 has a few issues preventing it from working with Warlock, but I have a working fork here: (https://github.com/sproctor/lich-5).
