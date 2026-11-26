# Candidate technical baseline

These are proposed defaults to validate and capture in ADRs. Do not add services or libraries without a clear need.

| Area | Candidate |
|---|---|
| Mobile | Expo + React Native + TypeScript; Expo Router |
| API | NestJS + TypeScript; REST; `/api/v1`; modular monolith |
| Identity | Supabase Auth (Google OAuth candidate); backend independently validates identity tokens and authorizes resources |
| Database | Neon PostgreSQL |
| ORM | Prisma |
| Media storage | Cloudflare R2, private objects, backend-authorized presigned access; direct client upload after authorization |
| Push | Expo Notifications; persisted notification records in DB |
| Server state | TanStack Query |
| Client state | Zustand |
| Forms | React Hook Form |
| Validation | Zod candidate (confirm approach and consistency in ADR) |
| Secure client storage | Expo SecureStore |
| Media selection/processing | Expo ImagePicker / ImageManipulator; Camera if needed |
| Maps | React Native Maps candidate; provider decision deferred |
| UI motion | Reanimated / Gesture Handler where justified |
| Icons | Lucide React Native |
| API testing | Jest, Nest testing utilities, Supertest |
| Mobile testing | Jest, React Native Testing Library; Maestro E2E later if appropriate |
| Logging | Pino |
| Scheduling | Nest scheduler/simple scheduled jobs initially; no queue infrastructure without a need |
| API docs | OpenAPI/Swagger |
| Monorepo | pnpm workspaces; avoid unnecessary monorepo framework initially |
| Hosting | Render candidate; evaluate free-tier constraints before relying on it |

## Separation of services
Supabase Auth, Neon Postgres, and R2 are independent services. Auth usage does not imply using Supabase database or storage.

## Architecture defaults
- Modular monolith; well-separated modules, not microservices.
- REST rather than GraphQL for initial API.
- Couple-space membership is an authorization boundary.
- Media binaries belong in private object storage; DB holds metadata and references.
- Use real PostgreSQL for meaningful integration tests.
- Avoid Redis, background queue services, and other infrastructure until use cases justify them.
- CI/CD is deferred; local test and verification tooling remains essential.

Validate and record consequential choices in ADRs.
