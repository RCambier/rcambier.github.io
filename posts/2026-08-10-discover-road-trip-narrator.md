---
aliases:
- /2026/08/10/discover-road-trip-narrator
categories:
 - project
date: '2026-08-10'
subtitle: a road trip guide that talks about what you are driving past
layout: post
published: true
title: Discover — a road trip narrator

---

[**Discover**](https://discover-on-the-road.vercel.app/) is a web app you put on
the dashboard while driving. It follows your GPS position and talks about the
places you pass: the region you are crossing, its history, and the landmarks
coming up along the road. The only setup is pasting in an OpenAI key.

::: {layout-ncol=3}
![](discover-monteriggioni.png)

![](discover-abbadia.png)

![](discover-settings.png)
:::

The main screen is a map. The circle around the car is the detection radius, the
trail behind it is where you have been, and the violet marker is the place
currently being talked about. The grey places were considered too: the named
ones might still get a mention later, the small dots were looked at and skipped.
There is no transcript, everything is spoken out loud.

## How it works

1. **Position.** The app waits for the GPS signal to settle before it starts
   talking, because a phone's first position fixes can be kilometres off.
2. **Research.** Every few kilometres it looks up the surroundings: reverse
   geocoding, Wikipedia in the local language first, Wikivoyage for the general
   character of an area, and a web search for the things encyclopedias are weak
   on.
3. **Choosing what to mention.** Each place gets a score based on how well known
   it is, how much there is to say about it, and how close you will pass. The
   bar is roughly what a good local guide would bother to mention. In the third
   screenshot you can add special interests: if you ask for railways, a small
   railway stop that would normally be skipped gets narrated.
4. **Timing.** A place is announced once, shortly before you can see it, and on
   the correct side of the road, based on your heading and speed. In the
   screenshots: *1.1 km · straight ahead*.
5. **Voice.** The narration is a single OpenAI realtime voice session. You can
   hold a button to ask a question, and the narrator can look something up while
   it answers.

## Practical details

Your OpenAI key stays in your browser and is only ever sent to OpenAI. An hour
of driving costs roughly $0.15 to $0.40. The other data sources (Nominatim,
Wikipedia, Wikivoyage) are free.

Because it is a browser tab, it cannot run with the screen off, so it keeps the
screen awake the way a navigation app does. There is also a native iPhone
version of the same engine.

The screenshots come from the app's built-in test drive, on the road from
Monteriggioni to Siena. The GPS is scripted and the voice server is faked so
that the same drive can be replayed during development, but the map and the
places are real.
