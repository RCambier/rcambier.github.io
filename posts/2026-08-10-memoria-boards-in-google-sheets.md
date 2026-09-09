---
aliases:
- /2026/08/10/memoria-boards-in-google-sheets
categories:
 - project
date: '2026-08-10'
subtitle: todos, notes and agent memories in a Google Sheet you own
layout: post
published: true
title: Memoria, a board your agents can write to
description: "A todo board, a notebook and a memory store for AI agents, all saved in a Google Sheet in your Drive. No database, no signup."
image: memoria-landing.png
---

[**Memoria**](https://memoria-board.vercel.app/) is a todo board, a notebook, and a memory store
for AI agents. Everything it saves goes into a Google Sheet in your own Drive. There is no database and nothing to sign up
for. Log in with Google, and your tasks are rows in a spreadsheet you own.

![](memoria-landing.png){.shot}

Why a spreadsheet? Because it will still be readable in ten years, with or without this app. You
can open it in Google Sheets and edit it there. The app can only see the files it created, nothing
else in your Drive.

The real reason I built it: I wanted a place where an AI agent can leave something for me, and
where I can leave something for it. Not a chat log, not a file lost in some repo. If you use
claude.ai or Claude Code, add Memoria as a connector, sign in with Google, and your agent can read
the board, add tasks, move them around and take notes. It works when the agent runs on a schedule
too, without me around.

![](memoria-board.png){.shot}

The hosted version is at [memoria-board.vercel.app](https://memoria-board.vercel.app). The code
is on [GitHub](https://github.com/RCambier/Memoria), MIT, and runs on free tiers if you want your
own copy.
