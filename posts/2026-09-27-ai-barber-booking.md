---
aliases:
- /2026/09/27/ai-barber-booking
categories:
 - project
date: '2026-09-27'
subtitle: making local barbers bookable by AI assistants
layout: post
published: true
title: AI Barber Booking, so your assistant can book the barber
description: "An MCP server that lets Claude or ChatGPT check a barber's free times and book an appointment, and a one-page pitch for the barbers and salons of Hackney Wick."
image: ai-barber-booking-banner.png
---

[**AI Barber Booking**](https://ai-barber-booking.vercel.app/) started with a simple question: can
I ask Claude to book me a haircut? Today, mostly no. An assistant can find a barber and give you a
link. It cannot see when the barber is free, and it cannot book.

So I built the missing piece: an MCP server with the tools an assistant needs. It can search shops,
read the menu and prices, check free times, hold a slot for ten minutes while you say yes, then
confirm, move or cancel the booking. To test it end to end I made up a salon, Atelier Nord, and
gave Claude one sentence: "Book me a skin fade near Hackney Wick on Tuesday afternoon." It booked
it. The first real test also found a bug: the hold lived in one server's memory, and the confirm
reached another server. Holds and bookings now live in Postgres, and the database refuses two
bookings for the same barber at the same time.

![](ai-barber-booking-demo.png){.shot}

Then the other half: the shops. I checked the public pages of 17 barbers and salons around
Hackney Wick and East Village. Most take bookings online on Fresha or Treatwell. None of them can
be booked by an AI assistant. The site is one page for them, with the same client asking the same
phone twice: without us, the booking goes next door; with us, it lands in their diary. Each shop
gets its own version of the page, with its name and what we already found about it.

Next is making setup take minutes: read the shop's services from its booking page, and use
calendar links, which every booking tool shares, so assistants only offer times that are really
free.

Try it with Claude Code:

```bash
claude mcp add --transport http ai-barber-booking https://ai-barber-booking.vercel.app/api/mcp
```
