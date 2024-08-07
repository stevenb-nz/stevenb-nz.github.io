---
layout: post
title:  Google Earth errors
date:   2020-02-15 23:33:30 +1300
categories:
---
I was running into two separate issues running Google Earth.

The first was a warning that "Citrix Receiver" would damage my computer.
The second was repeated request to access my Keychain.

Every attempt to find out what to do about the first problem led to assumptions that there was genuine malware being warned about (by Catalina), but none of the suggested ways to verify and deal with this led anywhere. It eventually turned out that, i) I had Citrix legitimately installed (from 'working from home' several years ago), and that this meant that there was a browser plug-in that Catalina was warning could be the malware when Google Earth tried to access it. So, first problem fixed by removing the Citrix plugin (that Chrome didn't appear to accessing, but Google Earth was). If I still needed to use Citrix to log in to a remote system, it appears that updating the version of Citrix Receiver would have fixed Catalina's issue with it, but haven't tried this to confirm it.

The second issue turned out to be a Keychain entry from Safari for a Google Earth login of some kind, that Google Earth didn't recognise as belonging to Safari. Solution - delete that entry from the Keychain (and only use the Google Earth app, not Safari, to use Google Earth in future).
