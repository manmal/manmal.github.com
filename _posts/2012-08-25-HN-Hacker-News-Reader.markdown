---
layout: post
title: HN - Hacker News Reader for Android
category: Design
tags: android design
year: 2012
month: 8
day: 25
published: true
---

I have been writing a Hacker News client for Android as a pet project, with the intention to eventually open-source it. Due to consulting and development work, I currently don't have the time to finish the app (refactor, thoroughly test, etc.) in the next weeks, so - i'll just release it now :)


<h2>Presenting HN Beta</h2>

<a href="/img/2012-08-25/hn-screenshots.png" target="_blank" style="border:none;"><img src="/img/2012-08-25/hn-screenshots.png" style="width: 600px; height: 370px;"></a>

<a href="#" class="button" style="font-size:40px; margin: 20px auto; width: 500px; padding:20px;">Get it at Google Play Store</a>
<a href="#" class="button" style="font-size:40px; margin: 20px auto; width: 500px; padding:20px;">Source at Github</a>

<h2>Why another HN reader app?</h2>

The existing HN Android clients I know are instable and don't look very good on my 4.0 phone. Most of them (or perhaps all) rely on external parsers which seem to break or go offline from time to time. So, I decided to build myself an app which parses Hacker News' HTML itself (thus working as long as HN itself is online). I also tried to make the app less cluttered and give it a beautiful UI. Judge for yourself if I managed to do that :)

<h2>Features</h2>

- Display frontpage posts
- Display comments
- Display stories in a view inside the app

<h2>More Planned Features</h2>

- Better story view (Back & Share icons, loading indicator)
- Improved comments view: http://dribbble.com/shots/627773-HN-screenshot-2-WIP
- Ability to provide login data and upvote posts
- Maybe: Ability to post comments
- Maybe: Switch to new posts on HN

<h2>Known issues</h2>

- HTML parsing will sometimes break for special cases - whenever you find that a view does not eventually load, please tweet me at @manuelmaly