# V1 direction and boundaries

This is a directional scope summary. Detailed behavior and acceptance criteria must be authored in feature specs.

## Candidate v1 capabilities
1. **Memories:** posts with multiple photos/videos, captions, notes, tags/categories, mood, memory date, optional location; partner reactions and comments.
2. **Albums:** title, description, cover; group memories without removing them from the primary feed.
3. **Relationship timeline and stats:** chronological history and meaningful statistics (e.g., days together, memories, albums, locations, letters, questions, completed bucket-list items).
4. **Timeline map:** location-bearing memories represented geographically; group/clustering at dense or repeated locations; map is a view of existing memories, not a separate memory system.
5. **Recaps:** periodic highlights that can include memories, locations, albums, letters, milestones, completed list items, and stats. Accessible after their initial presentation.
6. **Celebration letters:** letters for monthsaries/anniversaries; candidate reminder five days before; archive and reactions/comments, attachments may be supported. Surprise/unseen letter mechanics remain undecided.
7. **Question jars:** partner questions answered by both partners; shared answers and reactions/comments. Optional and spontaneous—no streak or mandatory daily engagement.
8. **Bucket lists:** shared experiences with title/description/image, category, optional target date, completion date, and ability to link a memory.
9. **Notifications:** in-app records and push delivery for relevant events; history, unread state, preferences/muting, deep links, device token management and cleanup. Push is not the source of truth.
10. **Account and relationship-space management:** onboarding, invite/acceptance, settings, privacy, export and deletion flows to be specified.

## Couple-space model
- Each v1 relationship space has exactly two members.
- Maye must support multiple relationship spaces in the service.
- No multi-space membership for an individual user in v1 unless separately approved.
- Invite links/tokens need expiry, revocation, and safe acceptance behavior.

## Explicit non-goals / deferred
- Public profiles, public feeds, follower systems, or social discovery.
- Microservices, GraphQL, or infrastructure complexity without a demonstrated need.
- Mandatory streaks, daily activity goals, or gamification pressure.
- CI/CD pipeline setup in the initial foundation phase (revisit when the project has code).
- Future feature ideas not included above; keep them out of v1 unless approved.

## Unresolved questions
Agents must identify and resolve these in specs/ADRs rather than assume: date and timezone semantics; recap generation and cadence; invitation lifecycle; letter visibility/surprise semantics; moderation/abuse and account recovery; location provider and privacy UX; export format; deletion and retention; backup/restore; notifications deduplication and delivery policy; video size/format limits; and any additional feature acceptance criteria.
