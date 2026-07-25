---
name: Subscribe to Credentially webhooks
description: Discover available webhook event types and manage subscriptions so an agent gets state-change notifications instead of polling.
api: openapi/credentially-webhook-openapi-original.json
operations: [getAvailableEventTypes, createSubscription, getSubscriptions, deleteSubscription]
---

# Subscribe to Credentially webhooks

Use this to receive state-change notifications (e.g. compliance or DBS status changed) instead of polling the REST API.

## Auth
Subscription management uses `Authorization: Bearer <API key>` (JWT) against `https://app.credentially.io/webhook-gateway`. Delivered callbacks carry their own Basic auth header that you define per subscription.

## Steps
1. Call `getAvailableEventTypes` (`GET /meta/events`) to get the authoritative list of event types and their payload fields.
2. Create a subscription with `createSubscription` (`POST /subscriptions`): set `callbackUrl` (must match `^https?://.+`), a `webhookName` (3-50 chars, `[A-Za-z0-9_-]`), a `password` (8-50 chars) used for Basic auth on your endpoint, and `eventTypes` (e.g. `PROFILE_COMPLIANCE_STATUS_CHANGED`, `PROFILE_DBS_STATUS_CHANGED`).
3. List existing subscriptions with `getSubscriptions` (`GET /subscriptions`); remove one with `deleteSubscription` (`DELETE /subscriptions/{id}`).

## Handling deliveries
- Callbacks arrive as `POST` to your `callbackUrl` with a Basic auth header = Base64 of `<webhookName>:<password>`. Verify it.
- Acknowledge within 15s with any `2xx`, or the callback is re-sent.
- Retries back off 30s, 60s, 120s ... up to 14 attempts.
- Treat callbacks as notifications only (fetch data via the REST API). Make your handler idempotent — ordering is not guaranteed and duplicates are possible.
