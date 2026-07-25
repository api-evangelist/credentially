---
name: Assign compliance packages and read check status
description: Assign compliance packages to a clinician and read their DBS, right-to-work, and reference status in Credentially.
api: openapi/credentially-gateway-openapi-original.json
operations: [getOrganisationCompliancePackages, getProfileCompliancePackages, assign, getProfileDbsChecks, updateProfileDbsCheck, getProfileRightToWork, getProfileReferences]
---

# Assign compliance packages and read check status

Use this to put a clinician onto the right compliance requirements and monitor their checks.

## Auth
`Authorization: Bearer <API key>` (JWT) against the regional gateway.

## Steps
1. List available packages with `getOrganisationCompliancePackages` (`GET /api/compliance-packages`).
2. Assign packages to a profile with `assign` (`POST /api/compliance-packages/{profileId}`), passing the list of package ids.
3. Read a profile's assigned requirements with `getProfileCompliancePackages` (`GET /api/compliance-packages/{profileId}`).
4. Monitor background checks:
   - `getProfileDbsChecks` (`GET /api/dbs/{profileId}`) for all DBS checks; `updateProfileDbsCheck` (`POST /api/dbs/{profileId}`) to create/refresh one from certificate details.
   - `getProfileRightToWork` (`GET /api/profile/{profileId}/right-to-work`) for the current right-to-work outcome.
   - `getProfileReferences` (`GET /api/profile/{profileId}/references`) for reference titles, dates, and status.

## Rules
- The public `profileId` maps to the upstream `employeePublicId` for DBS operations.
- For continuous monitoring, subscribe to `PROFILE_COMPLIANCE_STATUS_CHANGED` / `PROFILE_DBS_STATUS_CHANGED` webhooks (see the webhooks skill) rather than polling.
- Errors are HTTP-status only; `429` = rate-limited, back off.
