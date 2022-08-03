---
layout: post
title: "Warlock 3 is out of beta"
author: sproctor
date: 2022-08-03 17:38:00 -0400
categories: warlock update
---
Warlock 3.0.0 is out now! There are builds for Windows, Mac, and Linux.

Since the last post, I've improved the MacOS builds. Recent versions of MacOS require a developer license and signed builds, so I've delivered. They also want a notarized build (verified to be malware-free by Apple), so I've delivered that as well.

Performance of recent builds is much improved. Previously, each component (the little variable sections of the text windows) update would cause a [recomposition](https://developer.android.com/jetpack/compose/mental-model#recomposition). There's still some room for improvement, but the performance is now decent.

I had a bit of a misunderstanding on how the output tag worked. Warlock 2 would clear it on when it received a prompt. My Wrayth profile for some reason had a variable width font set for their "column" font. Finally, after some experimentation and confusion, you should see monospace fonts applied in more situations.

I also added a few features. Regular expressions are now supported in highlights (very similar to Warlock2). I added aliases and text alterations. Aliases allow you to replace text in command submissions with other text or variables. Text alterations allow you to change the window or content of text coming from the game server.

Please feel free to contact me if you have any suggestions. Use the contact link. The best way is is to join our slack channel, but email works too.

Happy gaming.
