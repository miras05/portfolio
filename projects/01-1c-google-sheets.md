# Nightly ERP → Google Sheets export

**Client:** state-owned enterprise, accounting on 1C:Enterprise (Kazakhstan edition)
**Status:** phase 1 runs on schedule on the client's database
**Code:** [1c-google-sheets-jwt](https://github.com/miras05/1c-google-sheets-jwt)

## Problem

Management wanted an up-to-date view of expenses in a Google Sheet every morning, broken down by
cost category, without anyone exporting reports from the accounting system by hand.

## What I built

- Every night at 02:00 the accounting system collects expenses from purchase documents.
- Each line is assigned a cost category automatically (cost of sales by business line,
  administrative, other). The classifier uses the warehouse and a keyword dictionary and is
  **about 91% accurate** on real data.
- Totals are aggregated by date and written to Google Sheets. The sheet is fully rewritten each
  run, so there are never duplicates.
- Export errors are written to the system's event log.

## The interesting part

External libraries couldn't be installed on the client's server, and Google APIs require a signed
token (JWT, RS256). So **SHA-256 and big-integer RSA are implemented directly in the 1C language**,
with no OpenSSL and no add-ins. The whole chain — signing, getting an access token, clearing and
writing the sheet — runs inside the ERP.

Scheduling is done with Windows Task Scheduler, because the platform's own scheduled jobs were
unavailable in this installation.

## Stack

1C:Enterprise 8.3 (BSL) · Google Sheets API v4 · Google service account · JWT RS256 ·
Windows Task Scheduler
