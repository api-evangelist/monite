---
name: monite-issue-and-send-invoice
description: Create a counterpart, draft a receivable (invoice), issue it, send it by email and fetch its PDF using the Monite Partner API.
api: Monite Partner API
generated: '2026-10-09'
method: generated
operations:
- post_auth_token
- post_counterparts
- post_receivables
- post_receivables_id_issue
- post_receivables_id_send
- get_receivables_id_pdf_link
- post_receivables_id_mark_as_paid
---
# Issue and send an invoice

1. `post_auth_token` — obtain an access token; send `Authorization: Bearer <token>` and `x-monite-version: 2024-05-25` on every call.
2. `post_counterparts` — create the customer (send `x-monite-entity-id` for entity-scoped calls).
3. `post_receivables` — create a draft invoice referencing the counterpart and line items.
4. `post_receivables_id_issue` — issue the draft (makes it immutable).
5. `post_receivables_id_send` — email the invoice to the counterpart.
6. `get_receivables_id_pdf_link` — retrieve the PDF link.
7. `post_receivables_id_mark_as_paid` — record payment received outside Monite.

Rules: errors follow the spec's error response schemas; rate limits per https://docs.monite.com/api/concepts/rate-limiting.
