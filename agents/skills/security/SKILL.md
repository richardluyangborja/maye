# Security and privacy

- Treat private memories, letters, locations and media as sensitive personal content.
- Every shared-data endpoint and object-access flow must enforce couple-space membership and resource authorization.
- Authentication is not authorization; validate identity and permissions server-side.
- Avoid leaking data via logs, errors, notification previews, analytics, URLs or client state.
- Validate inputs and uploads; consider rate limiting and abuse controls for invites, auth, upload and reactions/comments.
- Use private media storage, short-lived authorized access, and avoid permanent public URLs.
- Protect secrets and environment variables; don't commit them or include them in mobile builds.
- Assess deletion, export, retention, backup and recovery behavior.
- Include threat considerations and relevant security tests in feature work.
