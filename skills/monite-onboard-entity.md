---
name: monite-onboard-entity
description: Authenticate as a partner, create an entity (customer business) and subscribe to webhooks with the Monite Partner API.
api: Monite Partner API
generated: '2026-10-09'
method: generated
operations:
- post_auth_token
- post_entities
- get_entities
- post_webhook_subscriptions
- get_webhook_subscriptions
---
# Onboard an entity and subscribe to events

1. `post_auth_token` — partner-level token via client credentials.
2. `post_entities` — create the entity (organization or individual); `get_entities` to verify.
3. `post_webhook_subscriptions` — subscribe to object events (e.g. receivable, payable); `get_webhook_subscriptions` to list.
