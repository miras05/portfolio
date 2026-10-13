# AI lead bot + amoCRM

**Client:** countryside hotel (room bookings), later generalised into a reusable engine
**Status:** working demo
**Code:** [ai-leadbot-engine](https://github.com/miras05/ai-leadbot-engine)

## Problem

Managers spent time answering the same questions and copying requests into the CRM by hand.

## What I built

- A Telegram bot holds a natural conversation powered by an LLM and collects the request details:
  dates, guests, contacts.
- Once everything is collected, the bot **creates a contact and a deal in amoCRM** and attaches a
  note with the details.
- The engine is driven by niche configs: hotel, real estate, car leasing, clinic. A new niche is a
  new JSON file, no code changes.
- Model output is validated before it becomes a lead; if the CRM is down, the lead is saved to a
  file instead of being lost.

## Stack

Node.js · Telegraf · Groq (Llama 3.3 70B) · amoCRM REST API v4
