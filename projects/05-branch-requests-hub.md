# Branch requests hub

**Client:** company with 7 branches across Kazakhstan
**Status:** working prototype (code is private)

## Problem

Requests arrive in branch Telegram groups, by email and in Bitrix24. Management has no single view,
and urgent issues get lost in the noise.

## What I built

- Collects messages from three sources into one database: Telegram groups, email (IMAP, every 5
  minutes) and Bitrix24 (every 10 minutes).
- **A daily AI digest for management at 09:00** with priorities. Critical items automatically
  become tasks in Bitrix24.
- Search across all requests, customer cards, role-based access.
- Balances sources so that one verbose channel can't crowd the others out of the digest.

## Stack

Python · python-telegram-bot (job queue) · PostgreSQL 16 + pgvector · Docker · Groq (Llama) ·
Bitrix24 REST · IMAP
