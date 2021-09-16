---
layout: post
title: "Switch to Compose"
author: sproctor
date: 2021-09-16 09:04:00 -0400
categories: warlock update
---
Well, I never really had anything too interesting made with TornadoFX. It turned out that I wasn't very motivated to learn another UI toolkit and other priorities got in the way again. I had a decent PoC, but not much more. Which brings me to the point of this post, I'm happy to announce a slightly more complete Warlock using the new Compose Desktop UI.

If you're interested in this project, feel free to send me an email. The UI can use a lot of polish, and a lot of features are missing. Implemented so far: rudimentary scripting support, framework for parsing the StormFront protocol, compass/vitals/hands views. Big missing items: highlights, StormFront streams, status indicators.

Warlock2 offered some compatibility with Genie scripts. There was always something about their implementation that bothered me, and we never got it quite right. My plan for Warlock3 is to support compatibility with most StormFront scripts and add a bit of functionality on top. The StormFront script processor is completely forgiving and allows some really nasty stuff. I would like to give notice about bad behavior rather than silently ignoring it. From Genie, we'll support gosub
and whatever else makes sense. Already, I've implemented a pretty powerful "if" parser that allows complicated expressions in "if". I want to add an ability to escape into the expression parser to allow the same capabilities in arbitrary places in the scripts. My question is which symbol to use that doesn't break compatibility with existing StormFront scripts.

That's all for now. I'm going to try to do some polishing and publish an alpha release when I have time.
