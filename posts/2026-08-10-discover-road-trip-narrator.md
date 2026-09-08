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
description: "Discover is a little app I built for road trips. You put your phone on the dashboard, and while you drive it tells you about the places you are..."
---

[**Discover**](https://discover-on-the-road.vercel.app/) is a little app I built
for road trips. You put your phone on the dashboard, and while you drive it
tells you about the places you are passing: the region, its history, the castle
on the hill you would otherwise drive straight past. All you need is an OpenAI
key.

::: {layout-ncol=3}
![](discover-monteriggioni.png)

![](discover-abbadia.png)

![](discover-settings.png)
:::

The screen is just a map. The violet marker is the place it is currently
talking about, and the grey ones are places it considered but decided were not
worth interrupting you for. There is nothing to read while driving, everything
is spoken.

## What it does while you drive

Every few kilometres it quietly looks up what is around you: Wikipedia, in the
local language because that is usually where the good articles are, travel
guides, and the web for the things encyclopedias miss. Then it decides what is
worth mentioning. The bar I aimed for is what a good local guide sitting in the
passenger seat would point out: famous enough, interesting enough, close enough
to the road.

You can also tell it what you care about in the settings. If you say you like
railways, it will happily talk about a small station that anyone else would
drive past in silence.

It tries to get the timing right too. A place is mentioned once, a little
before it comes into view, and it tells you which side to look. In the
screenshots: *1.1 km, straight ahead*.

And if something makes you curious, you hold a button and ask. It answers, and
looks things up if it needs to.

## The practical bits

Your OpenAI key stays on your phone and is only used to talk to OpenAI. An hour
of driving costs somewhere between 15 and 40 cents. Everything else comes from
free sources like Wikipedia.

It runs in the browser, so it keeps your screen on while it works, like a
navigation app does. There is also an iPhone version of the same thing.

One honest note about the screenshots: they come from the app's built-in test
drive, on the road from Monteriggioni to Siena. The car and the voice are
simulated so I could replay the same drive while building the app, but the map
and the places are real.
