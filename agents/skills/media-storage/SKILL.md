# Media storage

Candidate approach: private Cloudflare R2 objects with backend-authorized upload/download access and presigned URLs; validate in ADRs.

- Backend authorizes uploads and establishes permitted object keys and metadata.
- Client uploads directly to storage only after authorization; client never holds account-level storage credentials.
- Validate MIME type, size, and actual content where feasible; consider safe image/video processing.
- Design upload states, progress, retry, cancellation, incomplete uploads and orphan cleanup.
- Store metadata and object references in DB, not media binaries.
- Use private objects and short-lived access; authorization must be checked before issuing access.
- Plan thumbnail/preview generation and export/deletion lifecycle.
- Test access restrictions and failure behavior.
