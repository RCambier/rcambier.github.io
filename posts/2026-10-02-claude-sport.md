---
aliases:
- /2026/10/02/claude-sport
categories:
 - project
date: '2026-10-02'
subtitle: an iPhone sports app that knows the whole context
layout: post
published: true
title: Claude Sport, what to do next
description: "An iPhone app I am building that learns your sports history, your goals in your own words and your injuries, then suggests only the next one to three things to do."
image: claude-sport-banner.png
resources:
 - claude-sport-mascot.mp4
 - claude-sport-mascot.png
---

**Claude Sport** is an iPhone app I am building. The idea is that it knows the whole context: the
sports I did over the years, what I want now, in my own words, and my injuries and how they healed.
From that, it suggests only the next one to three things to do.

<video autoplay loop muted playsinline poster="claude-sport-mascot.png" aria-label="The Claude Sport mascot cycling, playing tennis, running, juggling a football, skipping rope, lifting weights and doing yoga" style="display: block; width: 100%; max-width: 400px; margin: 1.5rem auto; border-radius: 16px;">
<source src="claude-sport-mascot.mp4" type="video/mp4">
</video>

A small round mascot does the sports. Claude does the thinking.

No forms. I just tell it, by voice or in a sentence: "the knee is fine again", "I want to run with
friends when it is sunny".

<!-- screenshot: today-suggestions -> posts/claude-sport-today.png -->
<!-- screenshot: trends -> posts/claude-sport-trends.png -->
<!-- screenshot: activity -> posts/claude-sport-activity.png -->
<!-- When the three PNGs are in posts/, replace the three lines above with:
::: {.phone-shots layout-ncol=3}
![](claude-sport-today.png)

![](claude-sport-trends.png)

![](claude-sport-activity.png)
:::
-->

It reads from many places, from the watch to the weather to an old email from the physio. The data
stays on the phone and is not stored anywhere else. To think, it sends a written summary to Claude,
through a small relay that passes it on without keeping or logging it.

It is in early testing on TestFlight, and for now I am the only tester.
