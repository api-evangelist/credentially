---
name: Onboard a clinician profile
description: Create a clinical staff profile in Credentially, populate its custom fields, and confirm it exists before running checks.
api: openapi/credentially-gateway-openapi-original.json
operations: [createProfile, updateProfileFields, getProfileByEmail, getProfileMetadata, loadProfiles]
---

# Onboard a clinician profile

Use this to add a new clinician to an organisation and get them ready for compliance checks.

## Auth
All calls use `Authorization: Bearer <API key>` (JWT). Keys are issued per organisation by a Credentially CSM. Pick the regional gateway matching the customer's data residency: EU/UK `https://app.credentially.io/gateway`, US `https://us.credentially.io/gateway`, CA `https://ca.credentially.io/gateway`.

## Steps
1. Call `getProfileMetadata` (`GET /api/profile/metadata`) to read the organisation's custom-field schema and available roles. Build your field payload against this schema — do not guess field ids.
2. Call `createProfile` (`PUT /api/profile`) with the clinician's core details and any custom fields. Respect the `create-profile` rate-limit bucket (25 req/1s).
3. If you need to set or change fields afterwards, call `updateProfileFields` (`PATCH /api/profile`) keyed by the profile's email.
4. Confirm with `getProfileByEmail` (`GET /api/profile/find`) or list via `loadProfiles` (`GET /api/profile`, paginated — read the `meta` block for paging).

## Rules
- On `409` the profile likely already exists — look it up with `getProfileByEmail` instead of recreating.
- On `429` back off; each operation has its own named rate-limit bucket.
- Errors are HTTP-status only (no problem+json body) — branch on status code.
