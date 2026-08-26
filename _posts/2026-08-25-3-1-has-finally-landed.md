---
layout: post
title: "3.1 has finally landed"
author: sproctor
date: 2026-08-25 22:20:00 -0400
categories: ["warlock", "update"]
---
Warlock 3.1.0 is out. It's been over a year since my last update here, and over 3 months since the
last stable release. With over 50 interim beta releases, 3.1.0 is the biggest update yet.

The biggest visible change is the window system. Game windows now live in a proper docking layout:
drag them around to rearrange, stack them into tabs, or detach one into its own OS window. Warlock
remembers where everything was, including windows you closed, and puts them back next launch.

Settings got a big rework too. Highlights, names, variables, macros, and the rest of your
per-character configuration moved out of the database into plain TOML files you can edit by hand.
Appearance settings were rewritten along the way: each window can be customized to override the
global settings in a predictable way. Thanks to Raidek for customizable window backgrounds. You
might need to do some Lich scripting to get them working though.

Scripts can now be written in Lua, which replaces the old JavaScript engine. Game panels have seen
a lot of improvement, including protocol implementation, font size, and scaling. Sound playback was
rebuilt on OpenAL and now works on Fedora and related distributions. And there's a pile of smaller
quality-of-life additions: reverse history search, find-in-window, per-character command history, a
reconnect button, auto-connect to your last character, and support for .sal launch files.

Under the hood, a lot of this release went into performance. Highlight matching is indexed so big
highlight lists no longer slow down every line, and the text buffer was reworked so excessive scrolling
doesn't lock up the UI. Finally, the latest release of Compose (1.12) allowed me to fix the most
common crashes, which were related to selected text leaving the viewport.

Grab it from the new [download page](/download.html). Happy gaming.
