# EduPlatform

A multi-role Learning Management System (LMS) built as a technical
portfolio project — Next.js + NestJS + PostgreSQL monorepo.

## Prerequisites

- Node.js >= 20
- pnpm >= 9
- Docker Desktop (running)

## Getting Started

1. Clone the repository:

```bash
   git clone <repo-url>
   cd eduplatform
```

2. Install dependencies:

```bash
   pnpm install
```

3. Set up environment variables:

```bash
   cp .env.example .env
```

Default values work out of the box for local development.

4. Start Postgres and Redis:

```bash
   docker compose up -d
```

Verify both services are healthy:

```bash
   docker compose ps
```

5. Run the development servers:

```bash
   pnpm dev
```

## Project Structure

eduplatform/
├── apps/
│ ├── web/ # Next.js frontend
│ └── api/ # NestJS backend
├── packages/
│ └── shared/ # Shared Zod schemas + TS types
├── docker-compose.yml
└── turbo.json

See `docs/architecture.md` (coming soon) for the full API map and
routing structure.
