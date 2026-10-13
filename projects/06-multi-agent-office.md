# Multi-agent office assistant

**Client:** demo built at a company's request
**Status:** demo on test data (code is private)

## Problem

Show how several AI agents can take over different kinds of office routine, with one orchestrator
routing tasks between them.

## What I built

- **Email agent** triages incoming mail: topic, urgency, required action.
- **HR agent** answers HR questions asked in plain language, using ERP-style data.
- **Scan agent** recognises documents with OCR.
- **Orchestrator** decides which agent a request belongs to.
- Starts with a single Docker command and ships with tests.

## Stack

Python · FastAPI · Groq (Llama 3.3 70B) · Tesseract OCR · SQLAlchemy / SQLite · Docker Compose
