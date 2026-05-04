# Financy

Full-stack financial management application built as a final postgraduate project at Rocketseat Faculty of Technology.

## Project Goal

Financy allows each user to manage personal finances with authentication, transactions, and categories, while keeping data isolated per account.

## Monorepo Structure

This workspace uses Git submodules:

- `financy-server`: GraphQL API with Fastify, Apollo Server, TypeGraphQL, and Prisma
- `financy-web`: React + Vite web client with Apollo Client

If submodules are not initialized yet:

```bash
git submodule update --init --recursive
```

## Main Technologies

- Backend: Node.js, TypeScript, Fastify, Apollo Server, TypeGraphQL, Prisma, SQLite, Vitest
- Frontend: React 19, TypeScript, Vite, Apollo Client, React Hook Form, Zod, Zustand, Tailwind CSS
- Quality: Biome, Vitest

## Challenge Requirements Status

- Account creation and sign in: implemented
- User can manage only their own transactions: implemented
- User can manage only their own categories: backend implemented, frontend UI still evolving
- Create transaction: implemented
- Delete transaction: implemented
- Edit transaction: implemented
- List transactions: implemented
- Create category: backend implemented, frontend UI still evolving
- Delete category: backend implemented, frontend UI still evolving
- Edit category: backend implemented, frontend UI still evolving
- List categories: backend implemented, frontend UI still evolving

## Prerequisites

- Node.js 20+
- pnpm
- Git with submodules initialized

## Run the Full Project

### 1. Backend

```bash
cd financy-server
pnpm install
cp .env.example .env.dev
# Add COOKIE_SECRET if it is missing in .env.dev
pnpm dev:generate
pnpm dev:migrate
pnpm dev
```

GraphQL API: `http://localhost:3333/graphql`

### 2. Frontend

```bash
cd financy-web
pnpm install
pnpm dev
```

Web app: `http://localhost:5173`

## Tests and Quality

- Backend tests: `pnpm test`, `pnpm test:watch`, `pnpm test:coverage`
- Frontend quality checks: `pnpm lint`, `pnpm check:biome`, `pnpm build`

## Notes

- Backend GraphQL schema is generated from registered resolvers.
- Frontend authentication flow and route protection are available.
- Dashboard, transactions, and categories UX in the frontend are under active iteration.
