# Real Integration Test

A Fastify + TypeScript backend with OAuth2 authentication and SQLite database support.

## Features

- **User Authentication** — Secure login and registration with password hashing
- **OAuth2 Login** — Social authentication via OAuth2 providers
- **SQLite Database** — Lightweight, file-based database with Drizzle ORM
- **TypeScript** — Fully typed codebase for better developer experience
- **API Validation** — Runtime schema validation with Zod

## Tech Stack

| Layer | Technology |
|-------|------------|
| Framework | [Fastify](https://fastify.dev/) |
| Language | TypeScript |
| Database | SQLite (via `better-sqlite3`) |
| ORM | [Drizzle ORM](https://orm.drizzle.team/) |
| Auth | JWT + OAuth2 + bcrypt |
| Validation | Zod |
| Testing | Vitest |

## Prerequisites

- [Node.js](https://nodejs.org/) >= 20
- npm (or pnpm / yarn)

## Getting Started

### 1. Install dependencies

```bash
npm install
```

### 2. Configure environment variables

```bash
cp .env.example .env
# Edit .env and fill in your secrets / OAuth credentials
```

### 3. Run database migrations

```bash
npm run db:migrate
```

### 4. Start the development server

```bash
npm run dev
```

The API will be available at `http://localhost:3000` (or the port defined in your `.env`).

## Available Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Start development server with hot reload |
| `npm run build` | Compile TypeScript to `dist/` |
| `npm start` | Run the compiled production build |
| `npm test` | Run tests once with Vitest |
| `npm run test:watch` | Run tests in watch mode |
| `npm run lint` | Lint the codebase with ESLint |
| `npm run db:generate` | Generate Drizzle migration files |
| `npm run db:migrate` | Apply pending database migrations |

## Project Structure

```
.
├── src/            # Application source code
├── tests/          # Test suites
├── docs/           # Documentation
├── .env.example    # Example environment variables
├── package.json
└── tsconfig.json
```

## License

MIT
