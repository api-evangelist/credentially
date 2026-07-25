---
name: Upload and verify a profile document
description: Upload a credential document to a Credentially profile, auto-fill its fields via OCR, then approve or reject it.
api: openapi/credentially-gateway-openapi-original.json
operations: [getDocumentTypes, uploadDocument, autoFillProcess, getDocuments, approve_1, reject, downloadFile]
---

# Upload and verify a profile document

Use this to attach a credential (e.g. registration certificate, ID) to a clinician and move it through the approval workflow.

## Auth
`Authorization: Bearer <API key>` (JWT) against the regional gateway.

## Steps
1. Call `getDocumentTypes` (`GET /api/documents/document-types`) to find the correct document type for the organisation.
2. Call `uploadDocument` (`PUT /api/documents/{profileId}`) to upload the file for the profile; this triggers processing. Watch for `413` (file too large).
3. Optionally call `autoFillProcess` (`POST /api/documents/auto-fill/process`) to OCR a newly uploaded file and return extracted fields, or `autoFillExisting` for a stored document. These share the `shared-intensive-write-limit` bucket (25 req/1s).
4. Review with `getDocuments` (`GET /api/documents/{profileId}`), which returns documents enriched with OCR fields.
5. Resolve the document: `approve_1` (`PATCH /api/documents/approve`) or `reject` (`PATCH /api/documents/reject`). Both are low-rate buckets (5 req/1s).
6. Retrieve a file's bytes with `downloadFile` (`GET /api/documents/download`) by file id.

## Rules
- Respect per-operation rate-limit buckets; `429` means back off.
- Treat document data as sensitive PII — the API key grants access to all staff documents.
