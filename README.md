# Portfolio — Miras Auganbayev

Commercial projects in AI integration and business automation, delivered for companies in
Kazakhstan. Client names are kept confidential. Where code can be shared, it has been stripped of
keys and client data and published as standalone repositories with tests and CI.

Telegram [@miras_au](https://t.me/miras_au) · mirasauganbayev@gmail.com

---

## Projects

| Project | Problem solved | Stack | Code |
|---|---|---|---|
| [Document recognition → ERP](projects/03-doc-recognition-1c.md) | Invoice photo → Gemini Vision → arithmetic checks → draft document in the ERP | Python, Gemini, Pydantic, OData, FastAPI | [doc-recognition-1c](https://github.com/miras05/doc-recognition-1c) |
| [WhatsApp booking bot](projects/02-whatsapp-booking-bot.md) | 24/7 bookings on the owner's own number, requests in Google Sheets | Python, FastAPI, WhatsApp Cloud API, Docker | [whatsapp-booking-bot](https://github.com/miras05/whatsapp-booking-bot) |
| [AI lead bot + amoCRM](projects/04-ai-leadbot-amocrm.md) | LLM holds the conversation, collects the lead, creates a CRM deal | Node.js, Llama 3.3, amoCRM API | [ai-leadbot-engine](https://github.com/miras05/ai-leadbot-engine) |
| [Nightly ERP → Google Sheets export](projects/01-1c-google-sheets.md) | Categorised expenses every night, with zero external dependencies | 1C:Enterprise (BSL), Google Sheets API, JWT RS256 | [1c-google-sheets-jwt](https://github.com/miras05/1c-google-sheets-jwt) |
| [Branch requests hub](projects/05-branch-requests-hub.md) | Telegram, email and Bitrix24 in one place, daily AI digest for management | Python, PostgreSQL + pgvector, Bitrix24 REST | [branch-requests-hub](https://github.com/miras05/branch-requests-hub) |
| Chat audit | Estimates hot leads and revenue lost to slow replies in messengers | Python (stdlib), SQLite, HTML dashboard | [chat-audit](https://github.com/miras05/chat-audit) |
| MAX web chat | Browser client for the MAX messenger via GREEN-API | React, TypeScript, Vite | [max-web-chat](https://github.com/miras05/max-web-chat) |
| [Multi-agent office assistant](projects/06-multi-agent-office.md) | Agents for email, HR queries and scans, plus an orchestrator | Python, FastAPI, Llama 3.3, OCR, Docker | private |

## Skills

- **AI integration**: LLMs in production (OpenAI, Gemini, Llama via Groq), schema-based data
  extraction, validating model output, niche-specific prompting.
- **Chatbots**: Telegram, WhatsApp Cloud API (including Coexistence), finite-state and LLM-driven
  dialogs.
- **Integrations**: CRMs (amoCRM, Bitrix24), ERP (1C:Enterprise via OData, BSL, HTTP services),
  Google Sheets with service-account auth, IMAP.
- **Backend**: FastAPI, queues and retries, idempotent webhook handling, PostgreSQL, SQLite.
- **Infrastructure**: Docker / Compose, VPS, Fly.io, GitHub Actions.

## How I work

I own projects end to end: discovery with the client, estimate and proposal, development, a demo
on the client's real data, launch, sign-off and support.
