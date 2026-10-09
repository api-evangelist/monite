---
name: monite-process-payable
description: Ingest a supplier bill as a payable, submit it for approval, approve payment and mark it paid using the Monite Partner API.
api: Monite Partner API
generated: '2026-10-09'
method: generated
operations:
- post_auth_token
- post_payables_upload_from_file
- post_payables
- get_payables
- post_payables_id_submit_for_approval
- post_payables_id_approve_payment_operation
- post_payables_id_mark_as_paid
---
# Process a payable (bill)

1. `post_auth_token` — get a bearer token; include `x-monite-version` and `x-monite-entity-id` headers.
2. `post_payables_upload_from_file` (OCR from a PDF/image) or `post_payables` (structured data) — create the payable.
3. `get_payables` — list/filter payables to confirm status.
4. `post_payables_id_submit_for_approval` — start the approval workflow.
5. `post_payables_id_approve_payment_operation` — approve the payable for payment.
6. `post_payables_id_mark_as_paid` — record the payment.
