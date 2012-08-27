---
layout: post
title: HN - Hacker News Reader for Android
category: Design
tags: android design
year: 2012
month: 8
day: 27
published: true
---

<a href="/img/2012-08-27/hn-screenshots.png" target="_blank" style="border:none;"><img src="/img/2012-08-27/hn-screenshots.png" style="width: 600px; height: 370px; display:block; margin: 0 auto;"></a>

<a href="#" target="_blank" class="button" style="font-size:40px; margin: 20px auto; width: 400px; padding:20px;">Get it at Google Play</a>
<a href="https://github.com/manmal/hn-android" target="_blank" class="button" style="font-size:40px; margin: 20px auto; width: 400px; padding:20px;">Source at Github</a>

Presenting HN Beta
------------------

I have been writing a Hacker News client for Android as a pet project, with the intention to eventually open-source it. Due to consulting and development work, I currently don't have the time to finish the app 100% in the next days, so - i decided to just release it now :)

Why another HN reader app?
--------------------------

The existing HN Android clients I know of are instable and don't look very good on my 4.0 phone. Most of them (or perhaps all) rely on external parsers which seem to break or go offline from time to time. I was really frustrated with the feed not loading 70% of the time, and comments not loading 90% of the time. 

So, I decided to build myself an app which parses Hacker News' HTML itself, and which will therefore work as long as HN is online (with some maintenance needed if they make structural HTML changes). I also tried to make the app less cluttered and give it a beautiful UI, with colors similar to HN's. Please judge for yourself if I managed to do that :)

Features
--------

- Display frontpage posts
- Display comments
- Display stories in a view inside the app

Planned Features
----------------

- Additions to story view (Back & Share icons, loading indicator)
- [Improved comments view](http://dribbble.com/shots/627773-HN-screenshot-2-WIP)
- Ability to provide login data and upvote posts
- Ability to switch between comments and story view
- Maybe: Ability to post comments
- Maybe: Switch to new posts on HN
- Maybe: Open & close comment thread levels (e.g., hide/show all subcomments of one certain comment)

Known Issues
------------

- HTML parsing will sometimes break for special cases - whenever you find that a view does not eventually load, please tweet me at @manuelmaly
- Loading a huge number of comments is sluggish on modern devices, and VERY sluggish on old devices. That can't be helped if the feed is parsed by the device itself.

Suggestions & Feedback
----------------------

Please tweet suggestions and feedback at [@manuelmaly](https://twitter.com/manuelmaly), or file an issue at the [Github Issues page](https://github.com/manmal/hn-android/issues).