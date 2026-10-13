# WhatsApp booking bot

**Client:** beauty/cosmetology practice
**Status:** built and verified in Docker, awaiting go-live on the client's number
**Code:** [whatsapp-booking-bot](https://github.com/miras05/whatsapp-booking-bot)

## Problem

The owner answers WhatsApp herself and loses clients while she is with a patient. She needed a bot
that replies 24/7, but without giving up her number: her phone must keep working as usual.

## What I built

- A bot on the official WhatsApp Cloud API in **Coexistence** mode: the same number works both in
  the phone app and through the bot. If the owner replies to a client herself, the bot goes quiet
  in that chat.
- Answers FAQs and collects a booking request: service, preferred time, name, phone.
- Requests land in a Google Sheet. The owner edits services, prices and FAQ answers there herself,
  with no developer involved.
- Recovers automatically after crashes and server reboots.
- Step-by-step installation guide written for any sysadmin.

## Stack

Python 3.12 · FastAPI · Pydantic v2 · httpx · WhatsApp Cloud API (Meta) · Google Sheets API ·
SQLite · Docker · Fly.io · ~1,800 lines of code
