---
layout: page
title: Privacy Policy
permalink: /privacy
---

*Last updated: 18 August 2026*

Warlock is an open source front end for Simutronics games, maintained by Sean Proctor. This
policy covers the Warlock application on all the platforms it ships for: Windows, macOS, Linux,
Android, and iOS.

## The short version

Warlock has no accounts, no advertising, and no analytics. Almost everything it stores — your
game credentials, your logs, your highlights and macros — stays on your own device. Three things
leave it: your login goes to Simutronics so you can play, crash reports go to Sentry so we can fix
bugs, and if you choose to connect a MUD Mobile account, your settings sync to that service.

## What stays on your device

Warlock keeps the following in its own storage on your computer or phone, and never sends it
anywhere:

- **Your game account username and password**, if you choose to save them.
- **Game logs**, if you enable logging.
- **Your settings** — highlights, macros, aliases, variables, named colors, window layout.
- **Your command history** and any scripts you write.

Warlock does not add its own encryption to this data. It is protected by whatever protection your
device already provides: iOS and Android encrypt an app's private storage, and on desktop the
protection is your operating system's file permissions and disk encryption, if you have it enabled.

Uninstalling Warlock, or deleting its configuration directory, removes all of it.

## Connecting to Simutronics games

When you log in, Warlock sends your account name and password to Simutronics' authentication
server (`eaccess.play.net`) and then connects to the game server you selected. This is the same
thing any game client does, and it is the only way to log in.

That information goes to Simutronics, not to us. We never receive it, never see it, and never
store it anywhere but on your own device. What Simutronics does with your account is covered by
their own privacy policy, not this one.

## Crash reports

When Warlock crashes, it sends a crash report to [Sentry](https://sentry.io), a third-party error
tracking service, so that the bug can be found and fixed. A report contains:

- the error and the stack trace that produced it
- the Warlock version and platform
- your operating system version and device model

Warlock's Sentry project is configured to discard the sending IP address and to scrub
personally identifying information, so neither is stored alongside the report. As with any
network request your IP address is visible in transit — that is how the report reaches Sentry
at all — but it is not retained.

Crash reports are not meant to carry your password, your game credentials, your game logs, or the
contents of what you type, and Warlock never sends any of that deliberately. One caveat worth
stating plainly: a report includes the error message that caused the crash, and Warlock spends most
of its time parsing text from the game, so a short fragment of game text or a character name can
occasionally end up inside such a message.

Reports are only sent from released builds — a build compiled from source for development does not
send them.

Sentry processes this data on our behalf. Their handling of it is described in
[Sentry's privacy policy](https://sentry.io/privacy/). There is currently no in-app switch to turn
crash reporting off; if you would like one, please say so on
[Discord](https://discord.gg/tBrDG425qB) or in a GitHub issue.

## MUD Mobile sync (optional)

Warlock can connect to [MUD Mobile](https://mudmobile.com), a separate service, so that your
settings follow you between devices. **This is off unless you turn it on** by entering a MUD
Mobile device token in Warlock's settings. If you never do that, nothing in this section applies
to you.

Once connected, Warlock uploads:

- your per-character settings files — highlights, macros, aliases, variables, and layout
- your game account name, character names, and character codes, so your characters can be listed

Warlock does **not** upload your password or your game key to MUD Mobile. Where a login secret is
needed to start a session, only a one-way hash of it is sent. Your connection list and the file
holding your MUD Mobile token stay on your device and are never uploaded.

You can stop this at any time by disconnecting your MUD Mobile account in Warlock's settings.

## Update checks (desktop only)

The Windows, macOS, and Linux versions of Warlock check for new releases by requesting release
information from GitHub. Like any web request, this makes your IP address visible to GitHub. No
information about you or your game account is included. The mobile versions do not do this; they
update through the App Store and Google Play.

## What Warlock never does

- No advertising, and no advertising identifiers.
- No usage analytics, tracking, or profiling.
- No location collection of any kind.
- No selling or sharing of personal information. There is nothing to sell.

## Children

Warlock is not directed at children under 13, and we do not knowingly collect personal information
from them. If you believe a child has sent us information through a crash report, contact us at
the address below and we will delete it.

## Your choices

Because Warlock stores your data on your own device, you control it directly: delete a saved
password in the account settings, clear your logs, or uninstall the app to remove everything. To
ask about data held in a crash report, or to request its deletion, email us — please include the
approximate date and the platform you were using so the report can be found.

## Changes to this policy

If this policy changes, the updated version will be posted on this page with a new date at the
top. Warlock is open source, so the change will also be visible in the site's commit history.

## Contact

Questions about this policy, or about privacy in Warlock generally, can go to
[sproctor@gmail.com](mailto:sproctor@gmail.com) or to
[our Discord](https://discord.gg/tBrDG425qB).
