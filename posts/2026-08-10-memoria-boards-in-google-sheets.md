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

[**Memoria**](https://memoria-board.vercel.app/) is a kanban board and a
notebook that saves everything into a Google Sheet in your own Drive. There is
no database and nothing to sign up for. You log in with Google, and your tasks
become rows in a spreadsheet you own.

![](memoria-landing.png)

The same sheet can also be used by AI agents. The board, your agents and the
spreadsheet always see the same thing, because the spreadsheet is the only
place where the data lives.

![](memoria-board.png)

## Why a spreadsheet

Because your data stays yours. Your tasks are just rows in a normal
spreadsheet. You can open it in Google Sheets and edit it there whenever you
want, and it will still be there, perfectly readable, in ten years, even if
this app disappears. The app can only see the files it created or the ones you
picked. It cannot look at anything else in your Drive.

## Letting your agents use it

This is the reason I built it. I wanted a place where an AI agent could leave
something for me, and where I could leave something for it, that is not a chat
log and not a file buried in some repo.

If you use claude.ai or Claude Code, you can add Memoria as a connector, sign
in with Google, and from then on your agent can read the board, add tasks, move
them around and take notes. It works even when the agent runs on a schedule,
without you there.

## Trying it

The easiest way is the hosted version at
[memoria-board.vercel.app](https://memoria-board.vercel.app). If you would
rather run your own copy, the code is open source and takes about fifteen
minutes to deploy, all on free tiers.

Source: [github.com/RCambier/Memoria](https://github.com/RCambier/Memoria). MIT.
