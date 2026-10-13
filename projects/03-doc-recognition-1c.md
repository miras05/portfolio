# Document recognition → ERP

**Clients:** small-business accounting department (prototype), demo for accounting firms
**Status:** working demo
**Code:** [doc-recognition-1c](https://github.com/miras05/doc-recognition-1c)

▶ [Demo video: from an invoice photo to a document in the ERP](https://github.com/miras05/doc-recognition-1c/blob/main/docs/demo.mp4)

## Problem

Accountants retype invoices and service acts into the accounting system by hand: supplier, line
items, quantities, prices, VAT.

## What I built

- The accountant sends a photo or PDF to a Telegram bot.
- Vision AI extracts the header and line items into strict JSON. Works with documents in Russian
  and Kazakh.
- The result is checked arithmetically (quantity × price, line totals vs. grand total, VAT, tax ID
  format), so model mistakes are flagged instead of silently saved.
- The bot creates a draft document in the ERP via OData and returns an Excel report.
- A mock ERP server with the same OData interface makes it possible to demo without access to the
  client's database.

## Stack

Python · python-telegram-bot · Google Gemini 2.5 Flash Vision · PyMuPDF · Pydantic · OData ·
FastAPI · openpyxl
