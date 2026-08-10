---
aliases:
- /2026/08/10/memoria-boards-in-google-sheets
categories:
 - project
date: '2026-08-10'
subtitle: kanban boards and notes stored in a Google Sheet you own
layout: post
published: true
title: Memoria — a board your agents can write to

---

[**Memoria**](https://memoria-board.vercel.app/) is a kanban board and a set of
markdown notes stored in a Google Sheet in your own Drive. There is no database
and no account to create: you sign in with Google, and the app reads and writes
rows in a spreadsheet you own.

![](memoria-landing.png)

Two things use that sheet: the web app, and an MCP server for coding agents.
Neither of them keeps its own copy of the data, so the board, your agents and
the spreadsheet always show the same thing.

![](memoria-board.png)

## Why a spreadsheet

Mostly because it keeps your data in your own hands. The tasks are plain rows
in a file you own. You can open the sheet and edit them there directly, and
they will still be readable in ten years even if this app is long gone. The app
itself stores nothing about you, and it can only access the files it created or
that you picked, never the rest of your Drive.

## Using it with agents

Every deployment also works as an MCP connector. Add it in claude.ai under
Connectors, or in Claude Code, sign in with Google, and your agent can list,
add, move and complete tasks on your boards, and do the same with notes. It
also works in scheduled and cloud runs.

This is the part I actually built it for: a place where an agent can leave
something for me, and where I can leave something for it, without it being a
chat log or a file in a repo.

## Practical details

You can use the hosted version at
[memoria-board.vercel.app](https://memoria-board.vercel.app), or fork the repo
and deploy your own with your own Google credentials. That takes about fifteen
minutes, all on free tiers.

Source: [github.com/RCambier/Memoria](https://github.com/RCambier/Memoria). MIT.
